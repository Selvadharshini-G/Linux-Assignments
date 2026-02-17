
## 1. Create a file and add executable permission to all users(user,group and others)
   
```
touch file1
chmod a+x file1
ls -l file1
```
## OUTPUT:

<img width="629" height="92" alt="image" src="https://github.com/user-attachments/assets/4dda80de-ab4c-4537-a4dd-a8ec84531515" />

## 2. Create a file and remove write permission for group user alone.

```
touch file2
chmod g-w file2
ls -l file2
```
## OUTPUT:

<img width="625" height="77" alt="image" src="https://github.com/user-attachments/assets/13829bcb-01eb-486b-b0dd-9101f959f4e9" />

## 3. Create a file and add a softlink to the file in different directory.(Eg: Create a file in dir1dir2/file and create a softlink for file inside dir1)

```
mkdir -p dir1/dir2
touch -p dir1/dir2/file
ln -s dir2/file dir1/file_link
ls -l dir1
```
## OUTPUT:

<img width="653" height="103" alt="image" src="https://github.com/user-attachments/assets/cebea8af-d795-43f5-833b-31bcc689a558" />

## 4. Use ps command with options to display all active process running on the system

```
ps -ef
```
## OUTPUT:

<img width="664" height="545" alt="image" src="https://github.com/user-attachments/assets/6bafadac-3d35-4b36-af00-eef2fb58776f" />

5. Create 3 files in a dir1 and re-direct the output of list command with sorted by timestamp of the files to a file

```
mkdir -p dir1
touch dir1file1 dir1/file2 dir1/file3
ls -lt dir1
ls -lt dir1 > dir1/file_list.txt
cat dir1/file_list.txt
```

## OUTPUT:

<img width="652" height="180" alt="image" src="https://github.com/user-attachments/assets/05c339df-f6e2-49c2-a035-3fe6f0a9f649" />




