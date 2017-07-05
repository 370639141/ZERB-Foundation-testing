# ZERB-Foundation-testing

## Install Foundation
1. Make sure you have [Node.js](https://nodejs.org/en/) and [SASS](http://sass-lang.com/install) installed.
2. Open Terminal and run `npm install --global foundation-cli`
3. If you run into any permission errors, try `sudo npm install --global foundation-cli`
4. Once installed successfully, go to the folder (e.g cd ~/Desktop/xxx/xxx) you want to create the project, and run `foundation new --framework emails`. it will ask you for a project name, which is used as the name of the folder to install in. After that, the project template will be downloaded, and the various dependencies installed. The entire process takes over a minute.
5. After your project has been installed, run `cd xxxxx`(name of the project just created). Then run: `npm start`

## How to Use Foundation
1. Make sure your project is running in the terminal. Every time you quit terminal or terminate the project, you should always go the the project directory and run `npm start` before making changes, or nothing will be compiled.
2. Working in src folder only. Here is a breakdown of the files in the src folder:
* assets/: Sass and image files.
* layouts/: Boilerplate HTML that wraps all of your emails.
* pages/: HTML files for emails.
* partials/: Reusable chunks of HTML that can be injected into pages.
3. The various HTML files, Sass files, and images inside of src will be automatically compiled to a new folder called dist/ (as in "distribution"), which contains the final HTML and CSS for your emails.
### HTML file
1. Under src/layouts/, there is a file called default.html. It is the bolierplate html that wraps all of the emails.
![Image](https://raw.githubusercontent.com/370639141/ZERB-Foundation-testing/master/assets/image/Screen%20Shot%202017-06-21%20at%2010.09.54%20AM.png)
2. Create a html file for email's body part in folder src/pages/.
3. Inky :sparkles:
  *  `<center>` : Used in html file to center image, button or any elements (instead of align="center" that we usually used in html).
  *  `<spacer>` : Used in html file to create white space. Set the size to the height of the space you need . I found that it is also very useful for creating borders within text. Define a class to the spacer, and define its max-width, border property in css file. Also put `<center>` tag around it.
  *  `<container>`,`<row>`,`<columns>`: Essencial feature of Inky.
  *  `<container>` : All emails should have a <container> element. This gives the email a maximum width for email clients on larger screens. It also orients the email in the center. A container is a full table, so it needs the tags <table>, <tr>, and finally <td>. The class .container goes on the <table>.
  *  `<row>` : A row is a <table> with a <tbody> and <tr>. Inside of this <tr>, you'll place each individual column. The <table> also has the class .row.
  *  original:
```
<table align="center" class="container">
  <tbody>
    <tr>
      <td>
        <table class="row">
          <tbody>
            <tr>
              <th class="small-12 large-12 columns first last">
                <table>
                  <tr>
                    <th>Put content in me!</th>
                    <th class="expander"></th>
                  </tr>
                </table>
              </th>
            </tr>
          </tbody>
        </table>
      </td>
    </tr>
  </tbody>
</table>
```
  *  with Inky: 
```
<container>
  <row>
    <columns>Put content in me!</columns>
  </row>
</container>
```

4. Partials. You can create partials under the folder src/partials, and insert them into the body part of the html. Partials could be applied to all the emails in the project.
