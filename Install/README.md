# PivotPi

PivotPi is a Servo Controller for the Raspberry Pi!

## Installing

You need internet access for the following step(s).

The quickest way for installing the PivotPi is to enter the following command:
```
curl -kL dexterindustries.com/update_pivotpi | bash
```
Or if you want to run the install script directly from the repository you can run:
```
bash install.sh
```

By default, the PivotPi package is installed system-wide and [script_tools](https://github.com/DexterInd/script_tools) is completely updated each time the script is ran.

An example using options appended to the command can be:
```
curl -kL dexterindustries.com/update_pivotpi | bash -s -- --user-local --no-update-aptget --no-dependencies
```

#### Command Options

The options that can be appended to this command are:

* `--no-dependencies` - skip installing any dependencies for the PivotPi. It's supposed to be used on each consecutive update after the initial install has gone through.
* `--no-update-aptget` - to skip using `sudo apt-get update` before installing dependencies. For this to be useful, `--no-dependencies` has to be not used.
* `--bypass-rfrtools` - skips installing RFR_Tools altogether.
* `--bypass-python-rfrtools` - skips installing/updating the python package for  [RFR_Tools](https://github.com/DexterInd/RFR_Tools).
* `--user-local` - install the python package for the PivotPi in the home directory of the user. This doesn't require any special read/write permissions: the actual command used is (`python setup.py install --force --user`).
* `--env-local` - install the python package for the PivotPi within the given environment without elevated privileges: the actual command used is (`python setup.py install --force`).
* `--system-wide` - install the python package for the PivotPi within the sytem-wide environment with `sudo`: the actual command used is (`sudo python setup.py install --force`).

Important to remember is that `--user-local`, `--env-local` and `--system-wide` options are all mutually-exclusive - they cannot be used together.
As a last thing, different versions of it can be pulled by appending a corresponding branch name or tag.

## Getting Help

Need help? We [have a forum here where you can ask questions or make suggestions](http://forum.dexterindustries.com/c/pivotpi-servo-controller-for-raspberry-pi).

See more at the [PivotPi Site](https://www.dexterindustries.com/pivotpi/)

## License

The MIT License (MIT)

PivotPi is a Servo Controller for the Raspberry Pi!
Copyright (C) 2016  Dexter Industries

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
