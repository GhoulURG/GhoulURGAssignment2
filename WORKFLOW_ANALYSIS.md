A. This means the workflow is triggered whenever code is pushed to the main branch.
B. 1. Checkout code which means it gets the repo code into the runner.
   2. Set up environment which means it configures the runtime 
   3. Build application which means it installs dependencies and compiles/prepares your app for deployment.
   4. Deploy application which means it Pushes the built app to the hosting environment.
C. It downloads your repository code into the GitHub Actions runner so the workflow can actually use it. Without this step, the runner would be empty, aka no project files, so the build and deploy steps wouldn’t have any source code to work with.
D. This step ensures the workflow has the right runtime tools to run your project. Without this, the runner might not know how to install dependencies or build your app.
E. Consistency: Every deployment runs the same way, reducing human error.
   Speed: Happens automatically on push to main.
   Verification: Ensures code builds successfully before deployment.
   Reproducibility: The workflow is version-controlled, so you can track changes to your deployment process.
F. If your deploy.yml is triggered only on main, then pushing to another branch would not trigger deployment. The workflow would just not run, so the changes you make would remain un-deployed until they’re merged into main.

