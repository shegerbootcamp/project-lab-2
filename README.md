# Project-lab-2 for cloudsheger devops student

Running the Script on all Servers

Now that we have the script and the servers ready and that we've added those servers in our servers.txt file we can run the following command to loop though all servers and execute the script remotely without having to copy the script to each server and individually connect to each server. 

```
for server in $(cat servers.txt) ; do ssh root@${server} 'bash -s' < ./remote_check.sh ; done
```
What this for loop does is, it goes through each server in the servers.txt file and then it runs the following command for each item in the list:

```
ssh root@the_server_ip 'bash -s' < ./remote_check.sh
```
You would get the following output:

