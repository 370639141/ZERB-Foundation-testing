# ZERB-Foundation-testing

## Install Foundation
1. Make sure you have Node.js installed.
2. Open Terminal and run `npm install --global foundation-cli`
3. If you run into any permission errors, try `sudo npm install --global foundation-cli`
4. Once installed successfully, go to the folder you want to create the project, and run `foundation new --framework emails`.
it will ask you for a project name, which is used as the name of the folder to install in. After that, the project template will be downloaded, and the various dependencies installed. The entire process takes over a minute.
5. After your project has been installed, run `cd xxxxx`(name of the project just created). Then run: `npm start`
6. You'll do all of your work in the src folder of your project. The various HTML files, Sass files, and images inside of src are compiled to a new folder called dist/ (as in "distribution"), which contains the final HTML and CSS for your emails.

## How to Use Foundation
1. Working in src folder only. 
2. Breakdown of the files in the src folder:
  * assets/: Sass and image files.
  * layouts/: Boilerplate HTML that wraps all of your emails.
  * pages/: HTML files for emails.
  * partials/: Reusable chunks of HTML that can be injected into pages.

