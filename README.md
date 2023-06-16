# Iran Geo IP Database

This repository contains a Python project that focuses on creating an MMDB (MaxMind DB) database for Iranian IP addresses. The purpose of this project is to generate a custom rule for direct access in the V2Ray VPN application.

## Repository URL

[https://github.com/Ilia-Abolhasani/iran-geo-ip](https://github.com/Ilia-Abolhasani/iran-geo-ip)

## Project Overview

The main objective of this project is to create an MMDB database by extracting Iranian IP ranges from the ip2location website and converting them to CIDR (Classless Inter-Domain Routing) notation. The generated database can then be utilized in the V2Ray VPN application to add a custom rule for direct access.

## File Structure

The repository consists of the following files and folders:

- `./data`: This folder contains the data files used for generating the MMDB database.
- `./result`: This folder stores the generated MMDB database file.
- `generate_by_eservices.ipynb`: This Jupyter Notebook file is responsible for extracting Iranian IP ranges from eServices.
- `generate_by_ip2location.ipynb`: This Jupyter Notebook file retrieves the Iranian IP range from the ip2location website, converts it to CIDR notation, and generates the MMDB dataset.
- `websites_urls_wildcard.ipynb`: This Jupyter Notebook file generates a list of Iranian website URLs to be used as wildcards in the VPN settings.

## Generating the MMDB Database

To create the MMDB database, follow these steps:

1. Run the `generate_by_ip2location.ipynb` notebook.
2. The notebook will fetch the Iranian IP range from the ip2location website and convert it to CIDR notation.
3. The resulting data will be used to generate the MMDB dataset.
4. The generated MMDB file will be saved in the `./result` folder.

## Installation

To install the required dependencies, follow these steps:

1. Install the `MaxMind-DB-Writer-python` package by running the following command:

   ```bash
   pip install -U git+https://github.com/VimT/MaxMind-DB-Writer-python

2. Install the maxminddb package by running the following command:
   ```bash
   pip install maxminddb

3. Install the additional Python packages by running the following command:
   ```bash
   pip install netaddr ipaddress pandas tqdm
   ```

These commands will ensure that you have the necessary dependencies installed for generating and working with the MMDB database. The additional packages (netaddr, ipaddress, pandas, tqdm) are required for various functionalities in the project.

Make sure to run these commands in your Python environment or virtual environment before using the project.




## Usage

Once you have the MMDB database file, you can incorporate it into the V2Ray VPN application to add a custom rule for direct access to Iranian IP addresses.

## Acknowledgments

The project utilizes the ip2location website ([https://lite.ip2location.com/iran-(islamic-republic-of)-ip-address-ranges?lang=en_US](https://lite.ip2location.com/iran-(islamic-republic-of)-ip-address-ranges?lang=en_US)) for retrieving Iranian IP ranges.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to modify and distribute it as per the terms of the license.
