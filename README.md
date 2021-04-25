# Fortran-with-Python_Linux

Fortran is a general-purpose, compiled imperative programming language that is especially suited to numeric computation and scientific computing.

In this Blog we'll understand how can we automate a Fortran program using python.

### Pre-Requisite :
* Fortran file.
* Python 3.*.
* Compiler that can compile fortran program like **gfortran** in Linux System. //Note: Compilers will compile your file depending your OS, program compiled on windows may not work for Linux sys.


### Compile // In Linux //:
* Run in terminal for creating compiled file **gfortran -c Program.FOR**

### Executable File:
* Run in terminal **gfortran Program.o -o RunProg.exe**

###### If you have more then one file to create a single application then you need to compile them seprately and then create Exe with all at once.

* **gfortran -c Program1.FOR**
* **gfortran -c Program2.FOR**
* **gfortran -c Program3.FOR**
---
* **gfortran Program1.o Program2.o Program3.o -o RunProgram.exe**


### Run Fortran Exe with python.
import subprocess, os
subprocess.run(['./RunProgram.exe'])

If your Exe requires some Inputs from User, then you can provide that in second parameter
Like: ```subprocess.run(['./RunProgram.exe', '1', '2', '4', ..])```

or You can save all the inputs into a file and pass the file to EXE using:
``` subprocess.run(['./screen3_linux.exe < {}'.format(dir_path + input_file)], shell=True) ```


