# OpenCobolIDE Install Manual

*This guide will walk you through the steps to install OpenCobolIDE on macOS.*

---

## Steps

### 1. Install Homebrew

Homebrew is a package manager for macOS that simplifies software installation.

1. Run the following command:
```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2. After installation, ensure Homebrew is ready to use:
```shell
brew doctor
```

---

### 2. Install GNU COBOL

1. Use Homebrew to install GNU COBOL:
```shell
brew install gnu-cobol
```

2. Verify the installation:
```shell
cobc -v
```

---

### 3. Install Python 3.9

1. Install Python 3.9 using Homebrew:
```shell
brew install python@3.9
```

2. Check the Python version to confirm:
```shell
python3.9 --version
```

> Warning: Only Python 3.9 is supported due to deprecation errors in later versions.

---

### 4. Set Up a Virtual Environment

1. Create a directory for your project, which will also contain example COBOL code:
```shell
mkdir ~/opencobolide_project
cd ~/opencobolide_project
```

2. Create a virtual environment:
```shell
python3.9 -m venv venv
```

3. Activate the virtual environment:
```shell
source venv/bin/activate
```

---

### 5. Install PyQt5

1. While inside the virtual environment, install PyQt5:
```shell
pip3 install PyQt5
```

---

### 6. Download OpenCobolIDE

1. Download the latest OpenCobolIDE package using wget
```shell
brew install wget
```
```shell
wget https://launchpad.net/cobcide/4.0/4.7.6/+download/OpenCobolIDE-4.7.6.tar.gz
```
You can just download using [here](https://launchpad.net/cobcide/4.0/4.7.6/+download/OpenCobolIDE-4.7.6.tar.gz)

---

### 7. Extract the OpenCobolIDE Files

1. Extract the downloaded file into a directory:
```shell
tar -xzvf OpenCobolIDE-4.7.6.tar.gz -C ~/opencobolide_project
```

---

### 8. Run OpenCobolIDE

1. Navigate to the extracted directory and run OpenCobolIDE with Python 3.9:
```shell
cd ~/opencobolide_project/OpenCobolIDE
```
```shell
python3 setup.py install
```

After that successful installation, you can run the ide using:
```shell
opencobolide
```

---

## Additional Notes

* Keep the virtual environment activated while working with OpenCobolIDE.
* Ensure you have example COBOL files in your project directory to test the setup.

---

*Enjoy coding with OpenCobolIDE! Happy Coding :)*

Feel free to contact me for assistance for any error encounters following the manual or if the download link isn't working.
