---
sidebar_position: 3
---

## Public API

Discover our public APIs for EVM File Uploader! These APIs provide convenient access to our services, allowing seamless integration into your applications. Feel free to explore and utilize these public APIs for your files on blockchain!

Public APIs are available at: [https://evm-api.epicmario71.com/](https://evm-api.epicmario71.com/)


# Usage of api.py

The `api.py` file located in the `tool` directory can be used to run the API server for BlockyFile. Follow the instructions below to execute the script and set the memory limit for contract size:

1. Make sure you have Python installed on your system.

2. Open a terminal or command prompt.

3. Navigate to the `tool` directory of the EVM-Data-Uploader project.

4. Run the following command to execute the `api.py` script:

   ```bash
   python api.py
   ```

   or

   ```bash
   python3 api.py
   ```

   Note: Use `python` or `python3` depending on your Python installation.

5. If you want to set the memory limit for contract size, use the `-m` flag followed by the desired memory limit. For example:

   ```bash
   python api.py -m 256
   ```

   This command sets the memory limit to 256 MB for contract size.

6. You can also use the `-s` flag to enable or disable statistics for future analysis. To enable statistics, use `-s True`, and to disable them, use `-s False`. For example:

   ```bash
   python api.py -s True  # Enable statistics
   python api.py -s False # Disable statistics
   ```

   This allows you to control whether statistics are collected and displayed in future analyses.


The API will be accessible at `http://127.0.0.1:8080`.

### Endpoints


1. A user-friendly web page where users can input an address and select a blockchain to either view the uploaded file or discover the blockchain on which the file is stored:
   - Endpoint: `/`
   - Example URL: `http://127.0.0.1:8080/`

2. To retrieve file data in JSON format:
   - Endpoint: `/json/`
   - Query Parameters:
      - `contract_address`: The address of the smart contract containing the file.
      - `chainid`: The chain ID of the Ethereum network (e.g., 5611 for Binance Smart Chain testnet).
   - Example URL: `http://127.0.0.1:8080/json/?contract_address=0x441122800E236D9b8eC34742D350CFD482D9607f&chainid=5611`

3. To retrieve a file (in base64 format) directly:
   - Endpoint: `/v1/`
   - Query Parameters:
      - `contract_address`: The address of the smart contract containing the file.
      - `chainid`: The chain ID of the Ethereum network (e.g., 5611 for Binance Smart Chain testnet).
   - Example URL: `http://127.0.0.1:8080/v1/?contract_address=0x441122800E236D9b8eC34742D350CFD482D9607f&chainid=5611`

4. To retrieve a password-protected file (in base64 format):
   - Endpoint: `/password/`
   - Query Parameters:
      - `contract_address`: The address of the smart contract containing the file.
      - `chainid`: The chain ID of the Ethereum network (e.g., 5611 for Binance Smart Chain testnet).
      - `password`: The password to decrypt the file data.
   - Example URL: `http://127.0.0.1:8080/password/?contract_address=0x441122800E236D9b8eC34742D350CFD482D9607f&chainid=5611&password=mysecretpassword`

### Additional Notes

- The API uses the specified chain ID to connect to different Ethereum networks.
- The API requires the contract address to be provided in lowercase hexadecimal format. It will automatically convert it to a checksum address if necessary.
- The API returns the file data in base64 format. It can also handle password-protected files if the password is provided in the URL.

Please note that this is just a basic implementation and should not be used in production without proper security measures. In a real-world scenario, consider implementing proper authentication, rate limiting, and other security practices to secure the API.

