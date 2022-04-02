This is docker file to create basic ssh-server
Command to create docker container

Buid command --> docker build -t ssh-server
Run container --> docker run -itd -P ssh-server

To connect with ssh-server container 
step 1: get the ip of host machine using "ifconfig" command
step 2: run docker ps and then see the port number 
step 3: run ssh command --> ssh user_name@host_ip -p port_number
