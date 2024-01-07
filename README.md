

run:

```bash

ansible-playbook ssh_user.yml -K

or

ansible-pull -U https://github.com/aydintb/create_ssh_users.git

```

----------------------------------------------------------------------------------

```bash

# group list:


groups aydin
groups deniz

getent group


# user list:

awk -F':' '{ print $1}' /etc/passwd
for user in $(getent passwd | cut -f1 -d: ); do echo $user;  done


```


yaml icimde tanimli useri karsi tarafta ssh uzerinden olusturur.
  
```bash

ssh ansible_robot@192.168.122.213 -i ~/.ssh/ansible 
ansible_robot@192.168.122.213: Permission denied (publickey).

```

-----

sil:

```bash

sudo userdel aydin -r
sudo userdel deniz -r
sudo userdel ansible_robot -r

sudo groupdel ansible_robot
sudo groupdel developer
sudo groupdel scala
sudo groupdel test
sudo groupdel math
sudo groupdel cpp
sudo groupdel english

sudo rm /etc/sudoers.d/aydin
sudo rm /etc/sudoers.d/deniz
sudo rm /etc/sudoers.d/ansible_robot

```

