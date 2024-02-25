# ftdprint - Python app to track sequentially generated files

``ftdprint``, of file-time-difference printer, was developed to be used with numerical simulation codes which generate output files periodically.
Typically with computational fluid dynamics codes, the solution data files corresponding to various vector and scalar fields
are written periodically to the disk by the solver.
When running such codes on supercomputers, the runs are limited by wall-time alloted by the job scheduler.
In such cases, it may be helpful to track how many files will be written by the code and to predict when the next file will be written,
based on the time intervals for the previously written files.
Assuming that this time interval does not change significantly, the app computes the approximate time required to write the next file
using a few shell commands available in most UNIX systems.

## Installing ftdprint

To install ``ftdprint``, you need to first clone the git repository into your local machine

`git clone https://github.com/roshansamuel/ftdprint.git`

The executable file ``ftdprint`` can be copied to some location included in the ``PATH`` environment variable, so that the command ``ftdprint``
is readily available at the command line.
If the file does not have executable permissions, it may be necessary to grant this permission using the ``chmod +x`` command.

The following Python modules are used by the app:

* ``sys`` - Used to parse command line arguments passed to the app
* ``numpy`` - All array manipulations are performed using NumPy
* ``datetime`` - This module effortlessly handles the date-time datatype for Python
* ``subprocess`` - This module is used to pass commands from Python to the shell

## License

``ftdprint`` is an open-source package made available under the New BSD License.

