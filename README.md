# Python-Based Port Scanne

This Python script is a multithreaded port scanner designed to scan open ports on a specified host. The script uses threads to efficiently perform port scanning and can handle high port ranges with customizable thread counts, start and end ports, and verbose output.

## Features

- **Multithreaded Scanning**: Uses multiple threads to speed up the scanning process.
- **Customizable Port Range**: Specify start and end ports for a targeted scan.
- **Adjustable Thread Count**: Control the number of threads to use for scanning.
- **Verbose Output**: Option to display the list of open ports as they are discovered.
- **Timeout Handling**: Configures socket timeout to avoid delays on unresponsive ports.

## Installation

Ensure you have Python 3 installed. No external libraries are required for this script.

To run the script, save it to a file (e.g., `port_scanner.py`) and make it executable:

```bash
chmod +x port_scanner.py

Usage

python3 port_scanner.py [options] <IPv4>

Options:

    <IPv4>: The IP address of the host to scan (required).
    -s, --start: Starting port number (default: 1).
    -e, --end: Ending port number (default: 65535).
    -t, --threds: Number of threads to use (default: 500).
    -V, --verbose: Verbose output to display open ports as they are found.
    -v, --version: Show the program version.

Examples

    Scan all ports on a host:

python3 port_scanner.py 192.168.1.2

Scan ports 20 to 1000 with 100 threads and verbose output:

python3 port_scanner.py -s 20 -e 1000 -t 100 -V 192.168.1.2

Display version information:

    python3 port_scanner.py -v

Output

    List of Open Ports: Shows all open ports discovered on the target IP.
    Time Taken: Displays the total time taken to complete the scan.

Example Output

Open port found: [22, 80, 443]
Time taken: 3.45 seconds

Requirements

    Python 3.x
    Internet Connectivity: Required if scanning external IPs.

Notes

    Running this script on a high port range with a large number of threads can significantly speed up the scanning process but may increase network load.
    Make sure to use this tool responsibly and only scan hosts you have permission to test.
