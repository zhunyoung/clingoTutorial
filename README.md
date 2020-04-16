# clingoTutorial
A tutorial for students to get started with Clingo

## Installation

### Easiest Way for Any System (Recommanded)
1. Install either Anaconda or Miniconda according to the following link
https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html

2. Create a virtual environment with python 3.6, and activate it. (Please notice the (py3.6) in your terminal after you activate it.)
```
conda create -n py3.6 python=3.6
conda activate py3.6
```

3. Install Clingo by copying and pasting the following command in a terminal prompt.
```
conda install -c potassco clingo
```

### Other ways to install Clingo
Below, we show how to install Clingo on different systems.
### Ubuntu
To install Clingo on Ubuntu

Copy and paste the following commands in a terminal prompt.
```
sudo apt-get update
sudo apt-get install gringo
```

### Mac OS
To install Clingo on Mac OS

1. Install brew: copy and paste the following command in a macOS Terminal prompt.
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

2. Install the Xcode Command Line Tools by executing the following command in a macOS Terminal prompt.
```
xcode-select --install
```
Then click “Install” to download and install the Xcode Command Line Tools.

3. Install Clingo by executing the following command.
```
brew install clingo
```

### Windows
To download Clingo on Windows system

1. Download Clingo (compressed in an .zip file) from the following link. This .zip file is also available in this repo.
https://github.com/potassco/clingo/releases/download/v5.4.0/clingo-5.4.0-win64.zip


2. Extract Compressed Folders in "clingo-5.3.0-win64.zip" to your preferred path, e.g.,
```
C:\Users\zyang90\Downloads\
```

## Hello World Example
Consider a Clingo program 
```
1{p(1..6)}.
```
which says that "p(1), p(2), ..., p(6) are possibly true AND at least one of them is true". Depending on your OS, you can follow the steps below to use Clingo to find all (or a specific number of) its stable models. 

### Linux or Mac OS
1. Save the Clingo program in a file, say "test.txt", in a folder and remember the path to this file. Say the path is as follows.
```
~\Downloads\test.txt
```
2. Open a terminal.
3. Execute the following command line to get all stable models of this Clingo program.
```
clingo ~\Downloads\test.txt 0
```
In the above command, 0 means that we require Clingo to output all stable models. If you don't put this 0, by default, Clingo will only output one stable model and terminate. You can also set this number to, say, 3 to let Clingo to output 3 stable models (if there exist) and then terminate.
### Windows
Suppose the path to the Clingo package is as follows. 
```
C:\Users\zyang90\Downloads\clingo-5.4.0-win64
```
You may use the following steps to execute Clingo on the example program.
1. Save the Clingo program in a file, say "test.txt", in the Clingo package folder. The path to the file "test.txt" is as follows.
```
C:\Users\zyang90\Downloads\clingo-5.4.0-win64\test.txt
```
2. Open a "Command Prompt".
3. cd to the Clingo folder. 
```
cd C:\Users\zyang90\Downloads\clingo-5.4.0-win64
```
4. Execute the following command line to get all stable models of this Clingo program.
```
clingo.exe test.txt 0
```
In the above command, 0 means that we require Clingo to output all stable models. If you don't put this 0, by default, Clingo will only output one stable model and terminate. You can also set this number to, say, 3 to let Clingo to output 3 stable models (if there exist) and then terminate.
