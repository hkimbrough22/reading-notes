# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 27 -->
[comment]: <> (https://developer.android.com/guide/components/activities/tasks-and-back-stack)
[comment]: <> (https://developer.android.com/training/data-storage/shared-preferences)

## Intents, Activities, and SharedPreferences

### Tasks and the Back Stack
- A task is a collection of activities that users interact with when trying to do something in your app. These activities are arranged in a stack—the back stack—in the order in which each activity is opened. 
- For example, an email app might have one activity to show a list of new messages. When the user selects a message, a new activity opens to view that message. This new activity is added to the back stack. Then, if the user presses or gestures Back, that new activity is finished and popped off the stack.
![Backstack](../diagram_backstack.png)

#### Managing Tasks
- The way Android manages tasks and the back stack, as described above—by placing all activities started in succession in the same task and in a last in, first out stack—works great for most apps and you shouldn't have to worry about how your activities are associated with tasks or how they exist in the back stack. However, you might decide that you want to interrupt the normal behavior. Perhaps you want an activity in your app to begin a new task when it is started (instead of being placed within the current task); or, when you start an activity, you want to bring forward an existing instance of it (instead of creating a new instance on top of the back stack); or, you want your back stack to be cleared of all activities except for the root activity when the user leaves the task.

- You can do these things and more, with attributes in the <activity> manifest element and with flags in the intent that you pass to startActivity().

- In this regard, these are the principal <activity> attributes that you can use:
  - `taskAffinity`
  - `launchMode` 
  - `allowTaskReparenting` 
  - `clearTaskOnLaunch` 
  - `alwaysRetainTaskState` 
  - `finishOnTaskLaunch`
  
- And these are the principal intent flags that you can use:
  - `FLAG_ACTIVITY_NEW_TASK`
  - `FLAG_ACTIVITY_CLEAR_TOP`
  - `FLAG_ACTIVITY_SINGLE_TOP`


### Save Small Key-Value Data
- If you have a relatively small collection of key-values that you'd like to save, you should use the SharedPreferences APIs. A SharedPreferences object points to a file containing key-value pairs and provides simple methods to read and write them. Each SharedPreferences file is managed by the framework and can be private or shared.

- `getSharedPreferences()` — Use this if you need multiple shared preference files identified by name, which you specify with the first parameter. You can call this from any Context in your app. 
- `getPreferences()` — Use this from an Activity if you need to use only one shared preference file for the activity. Because this retrieves a default shared preference file that belongs to the activity, you don't need to supply a name.


- For example, the following code accesses the shared preferences file that's identified by the resource string `R.string.preference_file_key` and opens it using the private mode so the file is accessible by only your app:
```java
Context context = getActivity();
SharedPreferences sharedPref = context.getSharedPreferences(
        getString(R.string.preference_file_key), Context.MODE_PRIVATE);
```


[BACK TO HOME](../README.md)