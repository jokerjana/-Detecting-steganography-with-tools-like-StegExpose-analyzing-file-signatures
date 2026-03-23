# Detecting-steganography-with-tools-like-StegExpose-analyzing-file-signatures
## AIM:
To detect hidden data using steganography detection tools like StegExpose and analyze file signatures for authenticity and manipulation.

## DESIGN STEPS:
### Step 1:
Install StegExpose or use the JAR version to detect steganography in image files.

### Step 2:
Run StegExpose on a directory of suspected image files using the command:

### Step 3:
Analyze file signatures using tools like file, binwalk, or xxd to check for inconsistencies or embedded content.

## PROGRAM:
- **Install and Verify Steghide Tool**
  ```bash
  sudo apt update
  sudo apt install steghide
  steghide --version 
  ```
- **Embed the Secret Message into the Image** 
  ```bash
  steghide embed -cf image.jpg -ef hidden.txt
  ```

- **Extract the Hidden Secret from Image and Verify the Extracted Message**
  ```bash
  steghide extract -sf image.jpg
   cat hidden.txt
  ```

- **Retrieve Information About the Embedded Data**
  ```bash
   steghide info image.jpg
  ```

- **Analyze File Signature**
  ```bash
    file image.jpg
    binwalk image.jpg
  ```
 
## OUTPUT:
### Install and Verify Steghide Tool
![image](https://github.com/user-attachments/assets/2654e9ee-be6b-4087-8f58-1071aef9b06f)


### Embed the Secret Message into the Image
![image](https://github.com/user-attachments/assets/232c715c-fc9d-4d25-9cef-6d7bcba1d32b)


### Delete Original Secret File
![image](https://github.com/user-attachments/assets/7f837277-da3e-4b22-abd1-2b0dfbd0810e)


###  Extract the Hidden Secret from Image
![image](https://github.com/user-attachments/assets/dc8bc93a-f1c3-4239-8a9e-db960cfd82f1)


### Verify the Extracted Message
![image](https://github.com/user-attachments/assets/62e8d489-5d95-4ff8-aa48-dde4ff1505b3)

### Retrieve Information About the Embedded Data
![image](https://github.com/user-attachments/assets/6688b699-7464-4b0d-8484-71d7254060c7)


### Analyze File Signature
![image](https://github.com/user-attachments/assets/6628fcf0-c56f-43ed-97f7-b5ec0656ddf5)

## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
