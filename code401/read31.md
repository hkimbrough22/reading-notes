# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 31 -->

[comment]: <> (https://developer.android.com/training/testing/espresso)

[comment]: <> (https://developer.android.com/studio/test/espresso-test-recorder)
## Espresso
Use Espresso to write concise, beautiful, and reliable Android UI tests.

```java
@Test
public void greeterSaysHello() {
    onView(withId(R.id.name_field)).perform(typeText("Steve"));
    onView(withId(R.id.greet_button)).perform(click());
    onView(withText("Hello Steve!")).check(matches(isDisplayed()));
}
```

Each time your test invokes onView(), Espresso waits to perform the corresponding UI action or assertion until the following synchronization conditions are met:

The message queue is empty.
There are no instances of AsyncTask currently executing a task.
All developer-defined idling resources are idle.
By performing these checks, Espresso substantially increases the likelihood that only one UI action or assertion can occur at any given time. This capability gives you more reliable and dependable test results.

[BACK TO HOME](../README.md)