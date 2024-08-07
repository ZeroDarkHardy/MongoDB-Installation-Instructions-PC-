# MongoDB Installation Guide for Students (PC Platform)

Author: Matt Hardy, August 6, 2024

This repository provides step-by-step instructions to help students install MongoDB on their PCs. Follow the instructions carefully to ensure a successful installation.

## Prerequisites

- A PC running Windows.
- Administrator access to install software.

## Installation Steps

### Step 1: Install MongoDB Community Server

1. Visit the following link to download the MongoDB Community Server installer (version 7.0.12):
   [MongoDB Community Server Installer](https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.12-signed.msi)
2. Run the downloaded `.msi` file to start the installation.
3. During the installation:
   - Choose the "Complete" setup type.
   
     ![complete_install.png](https://github.com/ZeroDarkHardy/MongoDB-Installation-Instructions-PC-/blob/main/images/complete_install.png)

   - On the "Service Configuration" screen, leave "Install MongoD as a Service" checked.
   
     ![service_config.png](https://github.com/ZeroDarkHardy/MongoDB-Installation-Instructions-PC-/blob/main/images/service_config.png)

   - Leave the data directory and log directory at their default settings.
   - Ensure the "Install MongoDB Compass" option is checked to install MongoDB Compass along with the server.
   
     ![compass_install.png](https://github.com/ZeroDarkHardy/MongoDB-Installation-Instructions-PC-/blob/main/images/compass_install.png)

   - Complete the installation to ensure MongoDB is installed at `C:\Program Files\MongoDB\Server\7.0`.

### Step 2: Install PyMongo

Check to see if you have pymongo installed in your dev Conda environment.

1. Launch the Anaconda prompt and run:
   ```sh
   conda activate dev
   ```

#### Check for PyMongo Installation:

2. Run the following code in your Anaconda prompt:
   ```sh
   conda list pymongo
   ```
3. If pymongo is installed on your machine, the command line will display the following information, although the versions may be different:
   ```sh
   (dev) MBP:~ User$ conda list pymongo
   # packages in environment at /opt/anaconda3/envs/dev:
   #
   # Name                    Version                     Build  Channel
   pymongo                   3.12.0            py310he9d5cce_0
   ```

4. If pymongo is not installed in your dev Conda environment, run the following in your Conda environment:
   ```sh
   conda install pymongo
   ```
   or
   ```sh
   pip install pymongo
   ```

### Step 3: Install Mongo Shell

1. Visit the following link to download the Mongo Shell:
   [Mongo Shell Zip File](https://downloads.mongodb.com/compass/mongosh-2.2.15-win32-x64.zip)
2. Extract the contents of the zip file.
3. Copy everything from inside the `bin` folder in the zip file into the `bin` folder within your MongoDB installation directory (e.g., `C:\Program Files\MongoDB\Server\7.0\bin`).

### Step 4: Install MongoDB Database Tools

1. Visit the following link to download the MongoDB Database Tools:
   [MongoDB Database Tools Zip File](https://fastdl.mongodb.org/tools/db/mongodb-database-tools-windows-x86_64-100.10.0.zip)
2. Extract the contents of the zip file.
3. Copy everything from inside the `bin` folder in the zip file into the `bin` folder within your MongoDB installation directory (e.g., `C:\Program Files\MongoDB\Server\7.0\bin`).

### Step 5: Add MongoDB to the Path Environment Variable

1. Open the Start Menu and search for "Environment Variables" and select "Edit the system environment variables".

    ![search_bar.png](https://github.com/ZeroDarkHardy/MongoDB-Installation-Instructions-PC-/blob/main/images/search_bar.png)

2. In the System Properties window, click the "Environment Variables..." button.

    ![env_variables.png](https://github.com/ZeroDarkHardy/MongoDB-Installation-Instructions-PC-/blob/main/images/env_variables.png)

3. In the Environment Variables window, find the `Path` variable under the "System variables" section and select it. Click "Edit...".

    ![variable_instructions.png](https://github.com/ZeroDarkHardy/MongoDB-Installation-Instructions-PC-/blob/main/images/variable_instructions.png)

4. Click "New" and add the path to the `bin` folder within your MongoDB installation directory (e.g., `C:\Program Files\MongoDB\Server\7.0\bin`).

    ![variable_instructions2.png](https://github.com/ZeroDarkHardy/MongoDB-Installation-Instructions-PC-/blob/main/images/variable_instructions2.png)
    ![file_path.png](https://github.com/ZeroDarkHardy/MongoDB-Installation-Instructions-PC-/blob/main/images/file_path.png)

5. Click "OK" to close all windows.

### Verifying the Installation

1. Open the Anaconda prompt.
2. Type `mongo` and press Enter. This should start the MongoDB shell.
3. Type `mongosh` and press Enter. This should start the MongoDB shell again.
4. Type `mongodump --version` and press Enter. This should display the version of the MongoDB Database Tools.

If you encounter any issues, please refer to the official MongoDB documentation or seek assistance from your instructor.

## Additional Resources

- [MongoDB Documentation](https://docs.mongodb.com/)
- [MongoDB University](https://university.mongodb.com/)
