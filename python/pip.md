# Pip

macOS comes with Python so there's a chance `pip` is already installed on your machine.

## Installation

```text
curl https://bootstrap.pypa.io/get-pip.py > get-pip.py
sudo python get-pip.py
```

To verify `pip` is installed properly run

```bash
pip --version
```

If it returns a version `pip` was successfully installed.

## Usage

Here are a few `pip` commands to get you started.

Install a Python package

```bash
pip install <package>
```

Upgrade a package

```bash
pip install --upgrade <package>
```

See what's installed

```bash
pip freeze
```

Uninstall a package

```bash
pip uninstall <package>
```

