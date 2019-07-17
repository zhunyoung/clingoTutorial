# clingoTutorial
A tutorial for students to get started with Clingo

## Installation and Hello World Example

### Easiest Way for Any System
1. Install either Anaconda or Miniconda according to the following link
https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html

2. Install Clingo by copying and pasting the following command in a terminal prompt.
```
conda install -c potassco clingo
```

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

1. Download Clingo (compressed in an .zip file) from the following link. This .zip file is also available from this repo.
https://github.com/potassco/clingo/releases/download/v5.3.0/clingo-5.3.0-win64.zip

2. Extract Compressed Folders in "clingo-5.3.0-win64.zip" to your preferred path, e.g.,
```
C:\Users\zyang90\Downloads\
```

To run Clingo on an example clingo program stored in "test.txt"

1. Write your clingo program in a .txt file in the clingo folder. The path to an example .txt file could be 
```
C:\Users\zyang90\Downloads\clingo-5.3.0-win64\test.txt
```
where the file "test.txt" contains the following rule.
```
1{p(1..6)}.
```

2. Open a "Command Prompt" and cd to the clingo folder. An example command line is as below, while you need to modify the path accordingly.
```
cd C:\Users\zyang90\Downloads\clingo-5.3.0-win64
```

3. Finally, you can execute the following command to find all stable models of the Clingo program stored in "test.txt".
```
clingo.exe test.txt 0
```
In the above command, 0 means that we require Clingo to output all stable models. If you don't put this 0, by default, Clingo will only output one stable model and terminate. You can also set this number to, say, 3 to let Clingo to output 3 stable models (if there exist) and then terminate.
