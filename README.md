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
![image](https://github.com/user-attachments/assets/bd29093d-28d6-42cd-9be3-b01cfcc95054)

### Embed the Secret Message into the Image
![image](https://github.com/user-attachments/assets/e2398682-3304-44b0-9969-fbece209a066)

### Delete Original Secret File
![image](https://github.com/user-attachments/assets/ebb0e137-d5b4-4978-8c04-fc07c2a0ac96)

###  Extract the Hidden Secret from Image
![image](https://github.com/user-attachments/assets/44ab3d26-56c5-4845-b4d0-25e7aa1c857c)

### Verify the Extracted Message
![image](https://github.com/user-attachments/assets/9d67f14e-272a-4dc7-8963-ebe08d10527b)

### Retrieve Information About the Embedded Data
![image](https://github.com/user-attachments/assets/1d2ed2e9-59d5-4541-8319-66c0c0be82f6)

### Analyze File Signature
![image](https://github.com/user-attachments/assets/292fdad7-cd87-4c07-bd43-d7808ad7c509)

## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.

