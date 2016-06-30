# Summary

**pywinfreeze** compiles Windows-compatible binaries on Linux.


# Use

~~~shell
./pywinfreeze /path/to/your/python/application.py
~~~

# About

**pywinfreeze** is based on [@GeneralCarto's instructions](https://milkator.wordpress.com/2014/07/19/windows-executable-from-python-developing-in-ubuntu/) for freezing python applications inside a [**virtual-wine**](https://github.com/htgoebel/virtual-wine) environment.

The script downloads and installs a temporary **vwine** environment containing **python 2.7**, **pip** and **pyinstaller**; then grabs your python application's package dependencies with [**pipreqs**](https://github.com/bndr/pipreqs) and freezes to a single `.exe` file. It creates two temporary directories while it's building your binary: `virtual-wine` and `venv_wine`.

The compiled binary is created in the directory where **pywinfreeze** was invoked.

*Note:* if your python script requires packages not available on **PyPi**, you'll need to ensure the source files are in your project directory.


# Requirements

* [**wine**](https://www.winehq.org/)
* [**SCons**](http://scons.org/)