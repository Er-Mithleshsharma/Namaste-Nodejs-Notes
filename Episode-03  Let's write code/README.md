## Namaste Node.js - Episode 3 Summary 
# Getting Started with Node.js: From Installation to Writing Your First JavaScript Code

##  Downloading and Installing Node.js

### Step 1: Download Node.js

1. Visit the [official Node.js website](https://nodejs.org/).
2. You will see two versions available for download:
   - **LTS (Long-Term Support)**: Recommended for most users as it is more stable.
   - **Current**: Includes the latest features but may be less stable.
3. Click on the **LTS** version to download the installer.

### Step 2: Install Node.js

1. Run the installer that you downloaded.
2. Follow the installation wizard:
   - Accept the license agreement.
   - Choose the installation path (default is usually fine).
   - Ensure that the option **"Add to PATH"** is checked (this allows you to use Node.js from the command line).
3. Complete the installation by clicking **Finish**.

### Step 3: Verify Installation

1. Open **Command Prompt** (CMD) or **Terminal**.
2. Type the following command to check the installed Node.js version:
   ```bash
   node -v
## 4.2. Writing Your First JavaScript Code in Visual Studio Code (VS Code)

### Step 1: Install Visual Studio Code
1. Visit the [Visual Studio Code website](https://code.visualstudio.com/).
2. Download the installer for your operating system (Windows, macOS, or Linux).
3. Run the installer and follow the prompts to install VS Code.

### Step 2: Open VS Code and Create a New File
1. Launch Visual Studio Code.
2. Open a new file by clicking on `File > New File` or use the shortcut `Ctrl + N`.
3. Save the file with a `.js` extension, for example, `firstScript.js`, by clicking on `File > Save As`.

### Step 3: Write Your First JavaScript Code
1. In the newly created `.js` file, type the following code:

    ```javascript
    console.log("Hello, World!");
    ```
2. Save the file.

### Step 4: Run the Code in VS Code Terminal
1. Open the integrated terminal in VS Code by clicking on `View > Terminal` or using the shortcut `Ctrl + ``.
2. Ensure that you are in the correct directory where your `.js` file is saved.
3. Run the code by typing the following command in the terminal:

    ```bash
    node firstScript.js
    ```
4. You should see the output `Hello, World!` printed in the terminal.

##  Writing and Running JavaScript Code in Command Prompt (CMD)

### Step 1: Open Command Prompt
1. Press `Win + R`, type `cmd`, and press `Enter` to open the Command Prompt.

### Step 2: Navigate to Your Project Directory
1. Use the `cd` command to change the directory to where you want to save your JavaScript file:

    ```bash
    cd path\to\your\directory
    ```

### Step 3: Create a JavaScript File
1. Create a new JavaScript file using any text editor (like Notepad) or directly from CMD:

    ```bash
    echo console.log("Hello, World!") > firstScript.js
    ```

### Step 4: Run the JavaScript Code
1. Execute the JavaScript file using Node.js by typing:

    ```bash
    node firstScript.js
    ```
2. The output `Hello, World!` should appear in the Command Prompt.
