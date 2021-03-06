# Abby
This is my personal Discord bot. I doubt anyone would ever have the need to
install this. However, here are some basic directions to get started.

Requires Python 3.10+

### Set-Up Environment
```
git clone https://github.com/thetallguyyy/abby.git
cd abby
python3 -m venv .venv
```

### Install Requirements
```
sudo apt install build-essential python3-dev libsystemd-dev
source venv/bin/activate
pip install -r requirements.txt
deactivate
```

### Configure
Rename default.config.py to config.py
```
cp default.config.py to config.py
```

Edit the following lines in config.py
```python
class Client(object):
    prefix = '' # the command prefix
    description = '' # bot description
    token = '' # bot api token
```

### Verify Configuration
```
sudo chmod +x ./abby.py
./abby.py
```

### Install
```
sudo chmod +x install.sh
sudo ./install.sh
sudo systemctl enable abby
```

### Verify systemd is Working
```
systemctl status abby
sudo journalctl -u abby
```
