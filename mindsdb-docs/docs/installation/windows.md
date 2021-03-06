
## Install using MindsDB installers

Install MindsDB on your Windows machine using an easy-to-use installler.

!!! tip "Download the installer"
    [MindsDB for Windows](https://mindsdb-installer.s3-us-west-2.amazonaws.com/mindsdb-installer/v2/windows/MindsDBInstaller_1.5.exe)

This installer will install Python3, MindsDB and MindsDB's dependencies, and create a shortcut on the desktop for starting MindsDB server.

!!! info "Unknown publisher warning"
    Currently, we are in a process of signing the Windows application, so in case you got a warning that the application is from `Unknown publisher`, click on a `Run anyway` button. If you experience additional issues using the Windows installer, please reach out to us on [GitHub](https://github.com/mindsdb/mindsdb/issues), or use the other installation options from bellow.

## Install using Anaconda

You will need <a href="https://www.anaconda.com/products/individual" target="_blank">Anaconda</a> or <a href="https://conda.io/projects/conda/en/latest/index.html" target="_blank">Conda</a> installed and Python 64bit version. Then open Anaconda Prompt and:

1. Create new virtual environment and install mindsdb:

    ```
    conda create -n mindsdb
    ```

    ```
    conda activate mindsdb
    ```

    ```
    pip install mindsdb
    ```

2. To verify that mindsdb was installed run:

    ```
    conda list
    ```

You should see a list with the names of installed packages.

## Install using pip

We suggest you to install MindsDB in a virtual environment when using `pip` to avoid dependency issues. Make sure your Python version is **>=3.6** and pip version **>= 19.3**.

1. Create new virtual environment called mindsdb:

    ```
    py -m venv mindsdb
    ```

    And, activate it:

    ```
    .\mindsdb\Scripts\activate.bat
    ```

2. Install MindsDB:

    ```
    pip install mindsdb
    ```

3. To verify that mindsdb was installed run:

    ```
    pip freeze
    ```
    
You should see a list with the names of installed packages.

!!! failure "Installation fail"
    Don't worry, simply follow the below bellow instruction which should fix most issues.

1. **Python 64** bit version is required. 


2. Depending on your environment, you might have to use **pip3** instead of **pip**, and **python3.x** instead of **py** in the above commands e.g

    ```
    pip3 install mindsdb
    ```

3. If you are using **Python 3.9** you may get installation errors. Some of the MindsDB's dependencies are not working with **Python 3.9**, so please downgrade to older versions for now. We are working on this and **Python 3.9** will be supported soon.

4. If installation fails when installing **torch** or **torchvision** try manually installing them following the simple instructions on their [official website](https://pytorch.org/get-started/locally/).

5. If you are using Windows, but are not using Anaconda or Conda, try installing one of them and running the installation from the **anaconda prompt**.

6. If you've previously installed mindsdb and are having issues upgrading to a new version, try installing with the command: 

    `pip install mindsdb --upgrade`

    If that still fails, try: 

    `pip install mindsdb --no-cache-dir --force-reinstall`

7. If none of this works, try installing mindsdb using the [docker container]() and create an issue with the installation errors you got on our  [Github repository](https://github.com/mindsdb/mindsdb/issues) and we'll try to review it within a few hours.