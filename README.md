# qrz.sh

This script queries the QRZ.com callsign database and returns
the result to the command line. A XML subscription plan with
QRZ.com is required for full functionality.

![screenshot](/screenshot.jpg?raw=true "screenshot")

# Installation

1. Clone the git to your local drive:
  ```
  wget https://github.com/phl0/qrz.sh.git
  ```
2. Extract the contents:
  ```
  tar -xzf qrz.sh.git && cd qrz.sh
  ```
3. Copy the script file _qrz.sh_ into a directory that is in your PATH variable
  * _/bin_ for system wide access
  ```
  cp qrz.sh /bin/
  ```
  * Or _/usr/local/bin/_ for your user only
  ```
  cp qrz.sh /usr/local/bin/
  ```
4. Copy the file _.qrz.conf_ into your home directory:
  ```
  cp .qrz.conf ~/
  ```
5. Set the correct file permissions (after navigating to the folder where you put the script):
  ```
  chmod u+x qrz.sh
  ```

# Dependencies

* curl
  ```
  sudo apt update && sudo apt install curl
  ```

# Configuration

Edit the file _~/.qrz.conf_ like this:
  ```
  sudo nano ~/.qrz.conf
  ```

  ```
  user=<your QRZ.com username - typically your callsign>
  password=<your QRZ.com password - NOT your API key>
  ```

# Usage

  ```
  # qrz.sh <callsign>
  ```
