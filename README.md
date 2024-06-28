
# Obfuscate Your JavaScript Code

This guide explains how to obfuscate your JavaScript code to make it less readable, enhancing the security of your GitHub Pages-hosted site.

## Prerequisites

- Node.js and npm installed on your local machine. You can download and install them from [Node.js official website](https://nodejs.org/).

## Step-by-Step Guide

### Step 1: Install Node.js and npm

First, make sure you have Node.js and npm installed. You can check this by running the following commands:

```sh
node -v
npm -v
```

If not installed, download and install Node.js from the [official website](https://nodejs.org/).

### Step 2: Install JavaScript Obfuscator

Open your terminal or command prompt and run the following command to install the JavaScript Obfuscator globally:

```sh
npm install -g javascript-obfuscator
```

### Step 3: Create Your Project Structure

Create the following directory and file structure:

```
/project-root
    ├── index.html
    ├── content.html
    └── assets
        ├── main.js
        └── styles.css
```

### Step 4: Write Your Original JavaScript (main.js)

Create and write your original JavaScript code in `main.js`:

```javascript
document.addEventListener("DOMContentLoaded", function() {
    fetchContent();
});

function fetchContent() {
    fetch('content.html')
        .then(response => response.text())
        .then(data => {
            document.getElementById('content').innerHTML = data;
        });
}
```

### Step 5: Obfuscate Your JavaScript Code

Navigate to your project's root directory in the terminal or command prompt and run the following command to obfuscate your JavaScript code:

```sh
javascript-obfuscator assets/main.js --output assets/main.obfuscated.js
```

### Step 6: Obfuscated `assets/main.obfuscated.js` (Example Output)

Below is an example output of the obfuscated `main.js` file:

```javascript
var _0x1234=["\x61\x31\x62\x32\x63\x33\x64\x34\x2E\x68\x74\x6D\x6C","\x74\x68\x65\x6E","\x74\x65\x78\x74","\x69\x6E\x6E\x65\x72\x48\x54\x4D\x4C"];document.addEventListener("DOMContentLoaded",function(){fetchContent()});function fetchContent(){fetch(_0x1234[0])[_0x1234[1]](response=>response[_0x1234[2]]())[_0x1234[1]](data=>{document.getElementById('content').innerHTML=data})}
```

### Step 7: Update `index.html` to Use Obfuscated JavaScript

Update your `index.html` file to reference the obfuscated JavaScript file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dynamic Content Loading</title>
    <link rel="stylesheet" href="assets/styles.css">
    <script src="assets/main.obfuscated.js" defer></script>
</head>
<body>
    <div id="content">
        <!-- দুঃখিত ইনস্পেক্ট এলিমেন্ট করার জন্য আপনি ইন্সপেক্ট করে এই কোড গুলো দেখতে পাবেন না ধন্যবাদ -->
        <!-- Sorry, you will not be able to see this code by inspecting the element. Thank you. -->
    </div>
</body>
</html>
```

### Step 8: Push Your Project to GitHub

Initialize a Git repository, commit your changes, and push your project to GitHub:

1. **Initialize Git (if not already initialized)**:

    ```sh
    git init
    ```

2. **Add your files**:

    ```sh
    git add .
    ```

3. **Commit your changes**:

    ```sh
    git commit -m "Initial commit with obfuscated JavaScript"
    ```

4. **Create a new repository** on GitHub and follow the instructions to add the remote repository:

    ```sh
    git remote add origin https://github.com/<username>/<repository>.git
    git push -u origin main
    ```

### Step 9: Enable GitHub Pages

1. Go to your repository on GitHub.
2. Go to the repository's settings.
3. Scroll down to the "GitHub Pages" section.
4. Select the source branch (usually `main` or `master`).
5. Click "Save".

### Final Output

Your site should now be live on GitHub Pages with the `index.html` file renamed to `content.html` and the JavaScript code obfuscated.

By following these steps, you can ensure that your JavaScript code is obfuscated and the content file's name is not easily recognizable, enhancing the security of your GitHub Pages-hosted site.


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
