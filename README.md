# GlokyPortScanner

GlokyPortScannar is a really fast tool to scan TCP ports implemented in Python. 

# Installation:

This program requires Python 3.9.

## Linux

1. clone the repository.

```bash
gi clone https://github.com/gl0ky/GlokyPortScanner.git
```

2. move to to 'GlokyPortScanner' directory.

```bash
cd GlokyPortScanner
```

3. Install requirements to make it works.

```bash
pip install -r requirements.txt
```

Now you should have the dependencies installed, run the program.

```bash
./GlokyPortScanner.py --help
```

you shuld see this:

```bash
Usage: GlokyPortScanner.py [OPTIONS] COMMAND [ARGS]...

Options:
  --help  Show this message and exit.

Commands:
  all-port-scan  Performs a scan to the full range of 65535 ports Args: ip...
  custom-scan    Performs a scan to the host to the different ports entered...
  default-scan   Performs a scan to the full of top 1000 ports Args: ip...
```

## Windows

1. clone the repository.

```bash
git clone https://github.com/gl0ky/GlokyPortScanner.git
```

2. move to to 'GlokyPortScanner' directory.

```bash
cd GlokyPortScanner
```

3. Install requirements to make it works.

```bash
py -m pip install -r requirements.txt
```

Now you should have the dependencies installed, run the program.

```bash
py GlokyPortScanner.py --help
```

you shuld see this:

```bash
Usage: GlokyPortScanner.py [OPTIONS] COMMAND [ARGS]...

Options:
  --help  Show this message and exit.

Commands:
  all-port-scan  Performs a scan to the full range of 65535 ports Args: ip...
  custom-scan    Performs a scan to the host to the different ports entered...
  default-scan   Performs a scan to the full of top 1000 ports Args: ip...
```

# Usage:

This program have 3 options to scan a host

## all-port-scan:

all-port-scan Basically it takes as a parameter the host to be scanned for example: scanme.nmap.org and performs a scan to the entire range of the existing 65,535 ports

```bash
C:\Users\cgarc\Projects\GlokyPortScanner>py GlokyPortScanner.py all-port-scan scannme.nmap.org

100%|███████████████████████████████████████████████████████████████████████████████████| 65535/65535 [00:33<00:00, 1938.13it/s]

[*] Scan is complete.

Host Scanned: scanme.nmap.org

Total ports scanned: 65535

Ports Found:

[*] Port 22 is open.
[*] Port 80 is open.
[*] Port 9929 is open.
[*] Port 31337 is open.

Time Elapsed: 33.84 seconds


C:\Users\gl0ky\Projects\GlokyPortScanner>
```
## custom-scan:

It takes as a parameter the host and the ports to be scanned for example: scanme.nmap.org 80,22,443 and performs a scan of the whole checking if these are open, the ports that are not open simply will not appear in the list

```
C:\Users\cgarc\Projects\GlokyPortScanner>py GlokyPortScanner.py custom-scan scannme.nmap.org 80,22,443

100%|███████████████████████████████████████████████████████████████████████████████████| 3/3 [00:00<00:00, 3003.80it/s]

[*] Scan is complete.

Host Scanned: scannme.nmap.org

Total ports scanned: 3

Ports Found:

[*] Port 22 is open.
[*] Port 80 is open.

Time Elapsed: 0.03 seconds


C:\Users\cgarc\Projects\GlokyPortScanner>
```

## default-scan:

take as parameter the host to scan for example: scanme.nmap.org performs a scan to the top 1000 ports

```bash
C:\Users\cgarc\Projects\GlokyPortScanner>py GlokyPortScanner.py default-scan scannme.nmap.org

100%|███████████████████████████████████████████████████████████████████████████████████| 1000/1000 [00:00<00:00, 4427.36it/s]

[*] Scan is complete.

Host Scanned: scannme.nmap.org

Total ports scanned: 1000

Ports Found:

[*] Port 22 is open.
[*] Port 80 is open.
[*] Port 9929 is open.
[*] Port 31337 is open.

Time Elapsed: 0.25 seconds

C:\Users\cgarc\Projects\GlokyPortScanner>
```