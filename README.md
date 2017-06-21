# ZERB-Foundation-testing

## Install Foundation
1. Make sure you have Node.js installed.
2. Open Terminal and type `<npm install --global foundation-cli>`




If you run into any permission errors (EACCESS) on OS X or Linux, you can try prefixing the command with sudo.

Copy
sudo npm install --global foundation-cli

Once the CLI is installed on your machine, it’s super easy to fire up a blank Foundation for Emails project. Move into the folder you store your projects in, and then run this command:

Copy
foundation new --framework emails

The CLI will ask you for a project name, which is used as the name of the folder to install in. After that, the project template will be downloaded, and the various dependencies installed. The entire process takes over a minute.

Running the Server
After your project has been installed, run cd project, where project is the name of the project just created. Then run:

Copy
npm start
This will kick off the build process, which includes HTML parsing, Sass, image compression, and a server. When the initial build finishes, your browser will pop open a new tab pointing to your project. You'll be seeing a blank index.html file.

File Structure
You'll do all of your work in the src folder of your project. The various HTML files, Sass files, and images inside of src are compiled to a new folder called dist/ (as in "distribution"), which contains the final HTML and CSS for your emails. These are the files you'll upload to Litmus, Campaign Monitor, etc. for testing, or load into your email campaign service.

Here's a breakdown of the files in the src folder:
