### Git Assignment for DevOps Internship
*Objective:*
The goal of this assignment is to assess your proficiency in using Git for version control, collaboration, branching strategies, continuous integration, and handling complex scenarios.

# *Instructions:*
1. *Repository Setup:*
   - Fork the provided repository on Git Classroom.
   - Clone the forked repository to your local machine.
   - Set up a remote named upstream pointing to the original repository.
2. *Branching and Workflow:*(CLI is recommended. Do try in UI also.)
   - Implement a Git branching strategy using Gitflow:
     - Create a develop branch.
     - Implement a feature (a simple script) in a branch named feature/add-advanced-functionality.
     - Merge the feature branch into the develop branch.
     - Create a release branch named release/v1.0 from the develop branch.
     - Tag the release branch with version v1.0.
     - Merge the release branch into both main and develop branches.
3. *Conflict Resolution:*
   - Introduce a deliberate conflict in the feature/add-advanced-functionality branch.
   - Resolve the conflict using Git and document the resolution steps.
4. *Git Submodules:*
   - Add a submodule pointing to another public GitHub repository of your choice within the project.
   - Update the README to include instructions on how to initialize and update the submodule.
5. *Hooks and Custom Scripts:*
   - Implement a custom Git post-merge hook that triggers a script (post-merge-script.sh) whenever a merge occurs in the repository.
   - Ensure the script is executable and prints a message indicating a successful merge.
6. *Interactive Rebase:*
   - Perform an interactive rebase on the develop branch to squash three consecutive commits into a single commit.
7. *Documentation and README:*
   - Update the README with comprehensive instructions on the Git workflow used, including details about branching, submodule initialization, and any additional steps. 

*This assignment is designed to challenge participants with various Git scenarios commonly encountered in real-world development environments. Adjust it as needed to suit the specific focus areas of your DevOps internship*
