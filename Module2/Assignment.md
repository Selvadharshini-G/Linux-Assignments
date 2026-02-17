## 1.Use the appropriate command to list all files larger than 1 MB in the current directory and save the output to a file.

```
find . -maxdepth 1 -type f -size +1M
```
## OUTPUT:

<img width="648" height="39" alt="image" src="https://github.com/user-attachments/assets/e343b739-ad38-4459-bf47-60730b29749f" />

## 2. Replace all occurences of "localhost" with "127.0.0.1" in a configuration file named config.txt, and save the updated file as updated_config.txt.

```
sed 's/localhost/127.0.0.1/g' config.txt > updated_config.txt
```

## OUTPUT:

<img width="523" height="81" alt="image" src="https://github.com/user-attachments/assets/b6ef8b5d-155b-4314-9c36-7889059cf488" />

## 3. Use the appropriate command to search for lines containing the word "ERROR" in a log file but exclude lines containing "DEBUG". Save the results to a file named filtered_log.txt

```
ubuntu_eur337@EURLTP-337:~$ grep "ERROR" log.txt | grep -v "DEBUG" > filtered_log.txt
cat filtered_log.txt
```

## OUTPUT:

<img width="646" height="125" alt="image" src="https://github.com/user-attachments/assets/47bca20e-6258-4c44-bdb7-94fa8c006758" />

## 4. Write a code to identify the process with the highest memory usage and terminate it .

```
TOP_PROC=$(ps aux --sort=-%mem | awk 'NR>1 {if($1!="root" && $11!="systemd" && $11!="unattended-upgr"){print $2, $11; exit}}')
PID=$(echo $TOP_PROC | awk '{print $1}')
PROC_NAME=$(echo $TOP_PROC | awk '{print $2}')

if [ -z "$PID" ]; then
    echo "No safe process found to terminate."
    exit 1
fi
if kill -9 $PID 2>/dev/null; then
    echo "Process $PROC_NAME (PID: $PID) has been terminated."
else
    echo "Failed to terminate process $PROC_NAME (PID: $PID). Permission denied."
fi
```
## OUTPUT:

<img width="652" height="176" alt="image" src="https://github.com/user-attachments/assets/42cb3106-59af-4912-9c1e-2393ea3e08a5" />

## 5.  Use the networking tool command and print all the gateway available in a sorted manner.

```
ip route show | awk '/default/ {print $3}' | sort
```

## OUTPUT:

<img width="655" height="61" alt="image" src="https://github.com/user-attachments/assets/3ed969ce-1466-40e6-9b20-a2e191eb1e1d" />




