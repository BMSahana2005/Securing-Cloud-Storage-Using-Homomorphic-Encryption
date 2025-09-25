# Securing-Cloud-Storage-Using-Homomorphic-Encryption
Python-based system for secure and efficient cloud file storage. It converts text files to ASCII, encrypts them using the CKKS homomorphic encryption scheme (via the TenSEAL library), compresses the encrypted data with gzip, and then uploads the final, secure file to Dropbox. The method prioritizes both data privacy and storage efficiency.

**Features**

--Homomorphic Encryption: Uses the CKKS (Cheon-Kim-Kim-Song) homomorphic encryption scheme, provided by the TenSEAL library, to encrypt data. This allows for potential future computations on the data without ever needing to decrypt it, ensuring privacy.

--Data Compression: Encrypted files are compressed using Python's gzip module. This reduces the file size, leading to faster uploads and more efficient storage in the cloud.

--Secure Cloud Integration: The final compressed and encrypted file is uploaded to Dropbox using the Dropbox Python API, providing a reliable and secure off-site storage solution.

--ASCII Conversion: The process begins by converting the input text file into its numerical ASCII representation, which prepares the data for the encryption process.

**How It Works**

--The system follows a four-step workflow to process and store a file securely:

--File Conversion: A user-provided text file is read, and its characters are converted into their corresponding ASCII numerical values. This creates an intermediate plaintext file of numbers.

--Encryption: The ASCII values are then encrypted using the CKKS homomorphic encryption scheme with the TenSEAL library. The output is a highly secure, encrypted file.

--Compression: The encrypted file is compressed using the gzip module to reduce its size, optimizing it for storage and transfer efficiency.

--Cloud Upload: The final, compressed, and encrypted file is uploaded to a designated folder in a Dropbox account.

This process demonstrates a trade-off where increasing levels of security (ASCII conversion -> CKKS encryption -> compression/upload) require a corresponding increase in processing time.

**Requirements**

To run this project, you'll need:

--Python 3.x

--The tenseal library

--The gzip module (built-in with Python)

--The dropbox Python library

--A Dropbox account with a valid API access token

**Installation**

--Set up your Dropbox API token:

--Create an app on the Dropbox Developers site.

--Generate an access token.

--Update the DROPBOX_ACCESS_TOKEN variable in the script with your token.

**Contribution**

Feel free to open issues or submit pull requests to improve the project. Future work could include optimizing upload speed, exploring parallel processing, or integrating with other cloud platforms.
