# EX 2: Analysis-of-the-Disk-Structure-using-Sleuth-Kit
## AIM:
To analyze the disk structure of a given disk image using Sleuth Kit tools in Kali Linux.


## DESIGN STEPS:
### Step 1:
Obtain or create a disk image file (e.g., disk.dd) to analyze. Open the terminal in Kali Linux.

### Step 2:
Use Sleuth Kit tools like mmls, fsstat, and fls to examine the partition layout, file system details, and file listing.

### Step 3:
Interpret the output of the tools to understand the disk structure, including partitions, sectors, and files.

## PROGRAM:
Sleuth Kit Disk Analysis Commands
✅ Option 1: Create a Sample Disk Image (for Testing)

Let’s create a 10MB blank disk image and simulate file system activity:

```bash
cd ~/Downloads

# Step 1: Create an empty disk image
dd if=/dev/zero of=disk.dd bs=1M count=10

# Step 2: Format it with a file system (like FAT32)
mkfs.vfat disk.dd
```

## OUTPUT:
![477354004-1fd99c6a-91f6-4789-b74b-e7b07c6d320f](https://github.com/user-attachments/assets/bc557f91-e39f-42f8-b341-b83a76397566)


### Create Disk
![477354230-80c69dc9-7352-4580-a4bc-085e5cf1a097](https://github.com/user-attachments/assets/822fe0b0-45e4-4a61-a38d-a9d52b3c1ef3)


### mmls 
```bash
mmls disk.dd
```
### fls
```bash
fls -f fat -o 0 disk.dd
```

 <img width="1153" height="206" alt="477354360-fa803429-51a4-4e2b-b802-546372fac2a9" src="https://github.com/user-attachments/assets/8a3d248e-075f-44dd-8c4e-6a13193c1137" />

![477356173-ee6f0813-2aa2-46d4-b079-5aa60683047c](https://github.com/user-attachments/assets/fad95655-167b-4fe3-a7b2-cae394758786)

![477356194-52d268f1-faa9-48e6-b4a7-6e1c6da0f19d](https://github.com/user-attachments/assets/c5a78475-8b4d-477f-8c21-db7f9ec17f7a)


## RESULT:
The analysis was performed successfully using Sleuth Kit, and the disk structure was understood in detail.
