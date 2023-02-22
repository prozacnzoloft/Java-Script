
### Installation Process
Open the directory where you want to store your project in VS Code or similar code editors.

**1)** Create a folder named  `layout` and download the files from this repository. The file structure is as follows.
```
.(Base Directory)
|--layout
    |--index.html
    |-- css
        |--style.css
    |--js
	|--script.js
```
<br/>

**2)** Go back to the base directory and open Terminal in VS code and enter the following command to install `npm`

    npm init -y

Your folder will then have `package.json` file in it.

<br>

**3)** Then enter this command to install TailwindCSS, PostCSS(cli) and AutoPrefixer as devDependencies.

    npm install -D tailwindcss postcss-cli autoprefixer

<br>

**4)** Now, enter this command to create `tailwind.config.js` file.

    npx tailwindcss init -p
    
The `-p` adds the `postcss.config.js` file so you don't have to add it manually.

<br/>

**5)** Now you have to add the path in `tailwind.config.js`. This path indicates the files in your project where Tailwind will be implemented.
Copy this code into the `tailwind.config.js` file.

    module.exports = {
      content: [
        "./layout/*.{html,js}",
        "./layout/**/*.js"
      ],
      theme: {
        extend: {},
      },
      plugins: [],
    }
If you want to add more files like TS or JSX then you have to change this entry.
<br>
**6)** Now add `tailwind.css` to your root directory.
Now your folder structure will be as follows.

    .(Base Directory)
    |--node_modules
    |--package.json
    |--package-lock.json
    |--postcss.config.js
    |--tailwind.config.js
    |--tailwind.css
    |--layout
        |--index.html
        |-- css
            |-- style.css
        |--js
    	    |--script.js
In the newly created `tailwind.css` file, add the following code

    @tailwind base;
    @tailwind components;
    @tailwind utilities;
<br/>

**7)** If you don't have a npm script, then copy this snippet into the `package.json` file

    "scripts": {
        "dev": "postcss tailwind.css -o ./layout/css/style.css --watch"
      },
This code commands the postcss to watch the files indicated in `tailwind.config.js` , and every time a class gets added in those files, postcss will take the relevant tailwind code from `tailwind.css` and stores it in `./layout/css/style.css`.

You can edit the project from here on.
Use Live Server Extension on VS Code
