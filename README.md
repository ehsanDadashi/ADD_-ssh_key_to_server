# ADD_ssh_key_to_server
add and enable sshkey and keybase auth in client server auth

# Steps

# First create ssh key in your cliet
ssh-keygen -t rsa -b 4096

# copy your public key from client
 go to ==> C:\Users\ehsan\.ssh
 
       copy id_rsa.pub file content 
# copy your id_rsa.pub content to SERVER
 go to /home/user/.ssh/
 
       vim authorized_keys

       add your id_rsa.pub file content to authorized_keys file
# add configuration to your ssh config
go to /etc/ssh

        vim sshd_config
        
                PasswordAuthentication no
                
                PubkeyAuthentication yes
# restart SSH service
systemctl restart sshd

# add your private key to your client mobox term 
<img width="941" alt="Untitled" src="https://github.com/user-attachments/assets/a0dfc31b-7d43-4d42-ba17-30a18172631c">
