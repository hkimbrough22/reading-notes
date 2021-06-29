#Git Introduction

##What is Git?

- Git is a version control system. A Version Control System (VCS) allows you to revisit various versions of a file by recording changes. 
- Through version control, one can revert a file or project to a previous version, track modifications and modifying individuals, and compare changes
- This also allows developers collaborate and even work on same code at the same time and remedy issues quickly and efficiently.

## Control Systems
- Through the years, VCS have changed from Local VCS, to Centralized VCS, and finally Distributed VCS (DVCS).
- Each progression of the VCS addressed overarching deficiencies with the previous "model".
- With the DVCS, developers bypassed the potential single point of failure with the Centralized VCS, i.e. the server involved in storage.
- DVCS allows users to create mirrored versions of repositories that can be easily be placed on the server to replace any lost information.
- This is the main tool for devleoper collaboration and simultaneous workflows.

## How?
- Using **Git Commands**, the `git clone` function, and the "Add, Commit, Push" (ACP) process, developers are able to pull files from the GitHub source and edit it on their local system.
- This increases efficiency as third-party coding clients on local systems often have valuable features that fully enable developers.
- First, you'll need to pull your file from GitHub using `git clone [URL to code]`.

##Breaking Down ACP
- After adding the file to your system, navigate to it within your terminal and open your code editor.
- Once editions are done with the specific file, you need to upload it back into GitHub for the useful collaboration described earlier.
- To do this we:
1. `git add [filename.filetype]` - Adds the file to show it is ready for committing.
2. `git commit -m "*narravtive text of changes made*"` - Allows to add a narrative explanation of changes made. Useful for tracking changes done. Like a caption for each snapshot.
3. `git push origin main` - Syncs changes made on the local system with GitHub.

[BACK TO HOME](README.md)
