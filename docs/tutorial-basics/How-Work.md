---
sidebar_position: 1
---

# How EVM File Uploader Works

EVM File Uploader utilizes a unique approach to securely store and manage files.

## File Upload Process

1. Encoding: When uploading a file with EVM File Uploader, the file is first encoded into Base64 or the selected encoding format. This encoding ensures that the file's content is represented in a standardized format for further processing.

2. Chunking: Next, the encoded file is divided into smaller chunks of approximately 55KB each. This chunking process allows for efficient handling of large files and ensures smooth upload and storage operations.

3. Smart Contract: Each chunk of the file is uploaded and stored in a smart contract within the blockchain. These smart contracts serve as individual containers for the file chunks, ensuring their immutability and traceability.

4. File Consolidation: Once all the file chunks are uploaded, a separate smart contract is created to consolidate and reconstruct the original file. This smart contract brings together all the uploaded file chunks to recreate the complete file in its original format.

5. Decoding: Upon request, the consolidated file is retrieved from the blockchain and decoded back into Base64 or the selected encoding format, making it ready for download or further processing.

## File Management Functions

EVM File Uploader provides several file management functions to enhance user control and ownership:

- **Transfer Ownership**: As the file owner, you have the ability to transfer ownership of a file to another user.

- **File Deletion**: Only the file owner has the authority to delete a file from Blockchain. This ensures that files cannot be tampered with or removed by unauthorized parties. The deletion process permanently removes the file from the blockchain, providing an added layer of security and control.

These file management functions empower users to maintain control over their uploaded files, collaborate securely, and preserve the integrity of the decentralized file storage ecosystem.