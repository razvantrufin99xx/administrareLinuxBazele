# administrareLinuxBazele

Tutorial de administrare linux 



1.find name of user


uname


uname -a



2.mounting drives


mount


3.cine sunt eu


whoami


4.remote conenct


ssh root@10.10.193.196 pass user -->


5.ip addreses connected


ifconfig


6.data timp


date


uptime


7.print on screen or >> > << <


echo date 



8. create a var 


current_date=$(date)


9.help


man whoami


10.navigate thrue teh system


System Navigation


11.path to a directory 

print work directory


pwd



12. change dir 



cd 

cd..

cd desktop


13. list dir files and dirs 


ls 

la -a 

ls -la 

ls -R   

ls -r

ls -t 

ls -S 

ls -Sr

la -1

la -1r



14. free screen 


clear


15. tree view of disk dirs 


tree 

tree <dirname>


16.creare dir 


mkdir  <dirname>


17. creare fila 


touch file.txt



18. view inside a file 


cat <filename>


19. write inside a file  using > redirectare


echo "file info " > file.txt 




20. nano editor 


open fila in nano 


nano <fila>



21.move fila 


mv <fila1> <file2>




22. afisare head din fila 


head <fila>



23. afisare fila de la final 


tail <file> -n 5




24. cautare 


find  / -name john

find / -name john 2> dev/null



grep  /var/log/wm.log active

cat  /var/log/wm.log grep active -n 


locate "johm"



25. cautare si cu poermisii asupra fisierelor dreptui de citire scriere stergere modificare creare 


find / -perm 755


find / -perm -u=x


find / -type d -perm -u=x


26.permisiuni asurpa fileleor



27. change execution permision for a file 


chmod +x burp.json 

chmod -x burp.json

chmod +xw burp.json 


28.add permisiun ide grup 


chmod g+x burp.json 



29. sterge permisiun ide grup util - 


chmod g-x burp.json 


30. user 


31.add user 


sudo

useradd <name>


32.parole 


33.ce parole au 


passwd <username> <username>


 

34. set pass expired 


passwd -e johnsmith 


35. delet user 


deluser <username> 


36.sterge group


delgroup <username / gourpname>


37.adda user in group cu parola 


useradd <nameofuser> -p 'sueprman' 


38. list parole users 

cat etc/passwd 


39. add nou group de users  si adauga si useri 

groupadd <groupnaem> 

usermod -aG <groupname> <username>


40.se in what group apartien un user 


groups <username>


41.stergere din group a unui user 

groupdel <username>


42.schimba din grup in altul un user 


usermod -g <groupstart> <groupdest>


43.see user in a group 


getent group <groupnaem>

sudo touch /etc/group 

getent group <groupname> 

gpasswd -a <username> <groupname> 



44. afisare paroel si gruprui


cat /etc/group | grep <groupname>



45.get entries of groups 


getent group <groupname>


46.combinare add user, add user in group , modifiy permision in group, modif permision in group 


a. adaugare user nou 

useradd ALEX 


b. creare parola la user nou 

passwd ALEX 

 ...adaugare parola noua op 



c.fortare schimbare parola la o noua logare

 

passwd -e ALEX 


d.adaugare i ngroup user nou 


groupadd grouptech 


e. adaugare in group 


usermod -aG grouptech ALEX 


f. verif daca e in group 


getent group grouptech 


g. adaugare permisiuni in groupul x 


pas 1 : intra in direcotrul de group cu localizare inainte

	

locate /etc/group 

^C

cd /etc 

ls 

ls -l 

 

pas 2 : schimbare permisii de group si crearea unui nou folder ucp ermisiun idegroup 

 

chmod g+rw grouptech  


cd..

cd ~

cd ..

ls 

mkdir techusers

ls 


pas 3 : schimbare ownership is permisiuni de group 

chown  :techgroup  techusers 

ls -l 

chmod g+rw techusers 

ls -l 



47.remove directory 


rmdir  techusers 

ls -l 



48.delete totul inapoi


a.  groupul 

groupdel grouptech 


b. user 

userdel ALEX 


c. verifica daca ai sterg userul 

cat /etc/grup | grep ALEX 



