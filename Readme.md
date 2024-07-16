# Portable Python (Windows)

The instance of non virtualized Python that is not dependent on the system path and can run independently. You can move python portable anywhere on your computer or to another computer. You can have more than one instance of portable python running simultaneously on your system. You can also have the combination of traditionally installed Python and portable Python.

The barebone of the Python portable is relatively small. It is not more than 9Mb in the 7z archive.

## How to use

Download or clone this project adn run ``portablepython3-11-9.ps1``. By default ``portablepython3-11-9.ps1`` will setup Python 3.11.9 in the ``python_embedded`` folder.

You can use the terminal too, if you prefer:

```powershell
.\portablepython3-11-9.ps1
```

If you desire to change the version, please use the terminal with the `source` argument:

```powershell
.\portablepython3-11-9.ps1 -source "https://www.python.org/ftp/python/3.9.10/python-3.9.10-embed-amd64.zip"
```

Link for [Python versions](https://www.python.org/downloads/windows/)

If you desire to change the destination folder, use the terminal with the `destination` argument:

```powershell
.\portablepython3-11-9.ps1 -destination "C:\new-path\PortablePython\"
```

Note: Path to a directory should always end with `\` (back space)

## Install PIP

To install ``pip``, you should navigate to the ``python_embedded`` folder first:

```bash
cd ./python_embedded
```

Then, run the following command:

```bash
.\python get-pip.py
```

Note: You only need to do this once.

## Running PIP

To install new modules, you should navigate to the ``python_embedded`` folder first:

```bash
cd ./python_embedded
```

Then, run the following command:

```bash
.\python.exe -m pip install YOURMODULE
```


## Running Scripts

``From the root of this project``, watch the following example to run ``test.py`` inside of ``test_script`` folder:

```bash
.\python_embedded\python .\test_script\test.py
```

You should see `Hello World!` on the terminal


## List of libraries installed on the portable version

To see the list of libraries, you should navigate to the ``python_embedded`` folder first:

```bash
cd ./python_embedded
```

Then, run the following command:

```bash
.\python.exe -m pip list
```

## Saving the List of Installed Libraries

Navigate to the ``python_embedded`` folder first:

```bash
cd ./python_embedded
```

Then, save the list of installed libraries to a file:

```bash
.\python.exe -m pip freeze > ..\requirements.txt
```

Note: The ``requirements.txt`` file will be saved at the root of this project.

## Install Libraries from a requirements.txt

Navigate to the ``python_embedded`` folder first:

```bash
cd ./python_embedded
```

Then, execute:

```bash
.\python.exe -m pip install -r ..\requirements.txt
```

You can try with the ``requirements_test.txt`` file.

Note: `requirements.txt` must exist on the root of this project. Note that `you must be inside of the python_embedded folder`, because it needs ``importlib`` and it could trigger stderr message if doesn't find it. 