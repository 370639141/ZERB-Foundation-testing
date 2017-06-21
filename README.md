# ZERB-Foundation-testing

## Install Foundation
1. Make sure you have Node.js installed.
2. Open Terminal and run `npm install --global foundation-cli`
3. If you run into any permission errors, try `sudo npm install --global foundation-cli`
4. Once installed successfully, go to the folder you want to create the project, and run `foundation new --framework emails`.
it will ask you for a project name, which is used as the name of the folder to install in. After that, the project template will be downloaded, and the various dependencies installed. The entire process takes over a minute.
5. After your project has been installed, run `cd xxxxx`(name of the project just created). Then run: `npm start`

## How to Use Foundation
1. Working in src folder only. Here is a breakdown of the files in the src folder:
* assets/: Sass and image files.
* layouts/: Boilerplate HTML that wraps all of your emails.
* pages/: HTML files for emails.
* partials/: Reusable chunks of HTML that can be injected into pages.
2. The various HTML files, Sass files, and images inside of src will be automatically compiled to a new folder called dist/ (as in "distribution"), which contains the final HTML and CSS for your emails.
### HTML file
1. Under src/layouts/, there is a file called default.html. It is the bolierplate html that wraps all of the emails.
![Image](https://raw.githubusercontent.com/370639141/ZERB-Foundation-testing/master/assets/image/Screen%20Shot%202017-06-21%20at%2010.09.54%20AM.png)
2. Create a html file for email's body part in folder src/pages/.
3. Inky :sparkles:
*  I did not use all of element in Inky, because not all of them are good to use. Here is the list of elements that I used:
  *  `<center>` : Used in html file to center image, button or any elements (instead of align="center" that we usually used in html).
  *  `<spacer>` : Used in html file to create white space. Set the size to the height of the space you need. I found that it is also very useful for creating those lines within text. Simply change the width of the spacer and add a border bottom to it would create a nice line. And also put `<center>` tag around it.
  *  `<container>`,`<row>`,`<columns>`: Essencial feature of Inky. Basically just put `<row>` under `<container>` and `<columns>` under `<row>` instead of using a lot of table,tbody,th,tr,td,etc. 
```css 
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
