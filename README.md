# swamp-struggle
Two player PvP game set in the Bayous of Louisiana.

DAY-TO-DAY GIT WORKFLOW

1. UPDATE MAIN
   Save and close Unity. Commit any unfinished work before switching branches.

   git switch main
   git pull --ff-only origin main

2. CREATE A TASK BRANCH
   Create one branch per feature or fix.
   Replace chris/player-movement with your own name and task.

   git switch -c chris/player-movement

   Open Unity and work on your task.

3. COMMIT YOUR PROGRESS
   Save your Unity files. Check the changes, then stage and commit them.
   Only include files that belong to your task.

   git status
   git diff
   git add .
   git commit -m "Add player movement"

   Commit = save a checkpoint on your computer.
   Make small commits with clear messages.

4. PUSH TO GITHUB
   First push for your branch:

   git push -u origin chris/player-movement

   After later commits:

   git push

   Push = upload your commits to GitHub.
   Push before ending a work session.

5. GET YOUR TEAMMATE'S MERGED CHANGES
   Commit your work and close Unity.
   Stay on your task branch, then run:

   git fetch origin
   git merge origin/main

   If conflicts occur:
   - Open the conflicting files and resolve the changes together.
   - Remove any conflict markers and save the files.
   - Complete the merge:

   git add .
   git commit

   If there are no conflicts, Git normally completes the merge automatically.
   Reopen Unity, test the combined changes, then run:

   git push

6. OPEN A PULL REQUEST
   Once the task works, commit and push your changes.
   On GitHub, choose "Compare & pull request".

   Base:     main
   Compare:  your task branch
   Describe: what changed and how to test it
   Reviewer: your teammate

   If fixes are requested, commit and push them on the same branch.
   The existing pull request updates automatically.

7. REVIEW AND MERGE
   Your teammate reviews the changes and tests them where needed.
   Once approved:
   - Select "Squash and merge" on GitHub.
   - Delete the completed remote branch on GitHub.

8. UPDATE AND REPEAT
   With your current work committed and Unity closed:

   git switch main
   git pull --ff-only origin main

   Create a fresh branch for your next task.
   If continuing an existing task branch, update it using step 5.

TEAM RULES
- Keep main working. Use reviewed pull requests for changes.
- Use one branch per task.
- Coordinate before editing the same Unity scene or prefab.
- Commit .meta files with their assets.
- Move and rename assets inside Unity.
- Keep the Unity .gitignore; do not commit generated folders such as Library.
- Use the same exact Unity Editor version.
- Close Unity before switching branches, pulling, or merging.
- Never force-push shared branches.
