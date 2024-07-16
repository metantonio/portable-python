# Portable python

The instance of non virtualized Python that is not dependent on the system path and can run independently. You can move python portable anywhere on your computer or to another computer. You can have more than one instance of portable python running simultaneously on your system. You can also have the combination of traditionally installed Python and portable Python.

The barebone of the Python portable is relatively small. It is not more than 9Mb in the 7z archive.

## How to use

Download ``portablepython3-11-9.ps1`` in a folder and run it. By default ``portablepython3-11-9.ps1`` will setup Python 3.11.9 in the ``python_embedded`` folder.

On the terminal:

```powershell
.\portablepython3-11-9.ps1
```

## Install PIP

To install new modules, you should navigate to the ``python_embedded`` folder first:

```bash
cd ./python_embedded
```

Then, run the following command:

```bash
.\python get-pip.py
```


## Running PIP

To install new modules, you should navigate to the ``python_embedded`` folder first:

```bash
cd ./python_embedded
```

Then, run the following command:

```bash
.\python.exe -m pip YOURMODULE
```