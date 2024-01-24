---
sidebar_position: 2
---

## Requirements

Python 3.7.2+ support

## For Windows 

For Windows, you may need to install the following package: [vc_redist.x64.exe](https://aka.ms/vs/17/release/vc_redist.x64.exe).

## Usage

Before running the program, make sure to configure the `.env` file. Follow the steps below:

1. Rename the `.env.example` file to `.env`.
2. Open the `.env` file and enter your eth address and private key. To retrieve the private key from MetaMask, follow these steps:
   - Open MetaMask and click on the account icon in the top right corner.
   - Select "Account Details".
   - Click on the "Export Private Key" button.
   - Copy the private key and paste it into the `.env` file.


To run the program, you need to install the required dependencies using the following command:

```bash
pip3 install -r requirements.txt
```
After installing the dependencies, you can execute the program using the following command:

```bash
python main.py
```

or on linux:

```bash
python3 main.py
```

Please note that Python 3.7.2+ is required.

Once done, the GUI will open, allowing you to easily upload the file. Alternatively, you can use the CLI option provided below:

## Program Options

The program can be executed with the following flags:

- `-t`, `--time_out`: Timeout time with RPC (default: 1200)
- `-e`, `--encoding_type`: Encoding Type of the file. Valid options: base64, base64withpassword (default: base64)
- `-g`, `--gui`: Enable/Disable GUI. Valid options: True, False (default: True)
- `-i`, `--input`: Path of the file to upload (works only with `--gui False`)
- `-rpc`: RPC URL of the BlockChain (default: https://opbnb-testnet-rpc.bnbchain.org/)
- `-p`, `--password`: Password for base64withpassword encoding (default: Password)
- `-gasprice`: GasPrice for transaction in Gwai value (float)
- `chainid`: ChainID of the BlockChain 
- `convalidate`: Convalidate file after upload False/True (default: False)
- `saveoutput`: Save the output address in output.txt False/True (default: False)