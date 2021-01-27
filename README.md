# ListMap
Created by: Shane Young/x90skysn3k

Updated for Python3 by: Brent White/ @brentwdesign

# Description
Listmap was made to save time when parsing through nmap output. Listmap creates lists of IP's based on the ports you specify. Listmap can aid in creating lists of IP adresses with open ports that can be referenced by other tools. Listmap was created to save time, basically saving your fingers from typing so many 'cat' & 'cut' statements through your gnmap outputs.

# Installation

`python3 -m pip install argcomplete`

# Usage

Command: `python listmap.py -h`

## Examples

### Generate a list filtered by open ports

* all hosts (by IP address) 
* with open ports 3390,443,80,22,21 
* in NMap output file `nmapoutput.gnamp`
* prefix the output file name name with 'pentest'

```
python listmap.py --file nmapoutput.gnmap --port 3390,443,80,22,21 --prefix pentest
```

### Generate a list of all open ports for an IP list

* for the IP addresses 172.1.2.3 and 172.2.3.4
* no filter on ports
* in NMap output file `nmapoutput.gnamp`
* prefix the output file name name with 'pentest'

```
python listmap.py --file nmapoutput.gnmap --ip 172.1.2.3,172.2.3.4 --prefix pentest
```

### Generate a CSV of IPs and Open Ports

* CSV format
* using the NMap input file `nmapoutput.gnamp`

```
python listmap.py --file nmapoutput.gnamp --csv 
```
