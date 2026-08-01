# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
<img width="733" height="275" alt="image" src="https://github.com/user-attachments/assets/2ff7f9f5-34ef-4ab2-878d-1f2da6e6ba9a" />



cat < file2
## OUTPUT
<img width="994" height="237" alt="image" src="https://github.com/user-attachments/assets/26d53387-da71-4ad7-afd0-807784db02dc" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="421" height="61" alt="image" src="https://github.com/user-attachments/assets/02a6ba34-4f29-4964-ae4f-ce6aca94b152" />

comm file1 file2
 ## OUTPUT
<img width="1156" height="432" alt="image" src="https://github.com/user-attachments/assets/14fd8248-3f67-430d-ac67-87a39cba74a2" />

 
diff file1 file2
## OUTPUT
<img width="1147" height="407" alt="image" src="https://github.com/user-attachments/assets/148b8b4e-bd58-4334-9ab6-07ee8161fac8" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
<img width="870" height="162" alt="image" src="https://github.com/user-attachments/assets/5e8b46c9-729a-4f69-a154-bc636ea36459" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="616" height="181" alt="image" src="https://github.com/user-attachments/assets/71e6a118-17f2-4890-91b7-c1a8e7633884" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="902" height="185" alt="image" src="https://github.com/user-attachments/assets/ac909b48-2318-4b9a-823a-ec132d738ad5" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
<img width="944" height="78" alt="image" src="https://github.com/user-attachments/assets/5dbf2e39-2869-4152-88e4-47a9c91ae185" />



grep hello newfile 
## OUTPUT
<img width="969" height="69" alt="image" src="https://github.com/user-attachments/assets/fdffb176-5348-4ad0-8e1b-a905c11bb9fd" />




grep -v hello newfile 
## OUTPUT
<img width="885" height="180" alt="image" src="https://github.com/user-attachments/assets/338216bb-6453-4187-bcde-a41dc2e49fcf" />



cat newfile | grep -i "hello"
## OUTPUT




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="736" height="96" alt="image" src="https://github.com/user-attachments/assets/f4a8a78b-b388-4542-a63e-80b68a93dfd0" />




grep -R ubuntu /etc
## OUTPUT
<img width="554" height="95" alt="image" src="https://github.com/user-attachments/assets/a85583fb-c836-44a8-9b1b-cce2a7337454" />



grep -w -n world newfile   
## OUTPUT
<img width="1182" height="930" alt="image" src="https://github.com/user-attachments/assets/26508679-720c-4e3d-8f7b-73da3832631f" />


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="710" height="92" alt="image" src="https://github.com/user-attachments/assets/77ddeab3-5d85-4a27-8102-47c52b5c6042" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="542" height="91" alt="image" src="https://github.com/user-attachments/assets/5dfb2417-2810-4028-8ba2-4b1e6abe38a9" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="789" height="92" alt="image" src="https://github.com/user-attachments/assets/4fe3cd70-36a9-45cb-b44e-09951369cc76" />




egrep '(^hello)' newfile 
## OUTPUT



egrep '(world$)' newfile 
## OUTPUT
<img width="700" height="76" alt="image" src="https://github.com/user-attachments/assets/0275f8be-50e9-4a84-9c71-179c0a64c3cf" />



egrep '(World$)' newfile 
## OUTPUT
<img width="645" height="95" alt="image" src="https://github.com/user-attachments/assets/96269bbe-d11d-4187-95be-17225b3d8b60" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="698" height="70" alt="image" src="https://github.com/user-attachments/assets/775b44e1-9657-4e57-b98b-7c9814854da6" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="864" height="74" alt="image" src="https://github.com/user-attachments/assets/e83b6bdb-9d62-4a5c-845f-0209d99f0e4a" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="864" height="74" alt="image" src="https://github.com/user-attachments/assets/ec9996e6-c43a-4a03-82a0-50403559ef98" />



egrep 'Linux.*World' newfile 
## OUTPUT


egrep l{2} newfile
## OUTPUT
<img width="680" height="72" alt="image" src="https://github.com/user-attachments/assets/b060622e-aa07-4b99-884f-cfe61f0cb2c8" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="769" height="120" alt="image" src="https://github.com/user-attachments/assets/e33c3954-60ef-432a-b1f9-99ccfe8908f6" />



cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
<img width="952" height="70" alt="image" src="https://github.com/user-attachments/assets/54f22226-34c4-4197-b773-9e48f2740b0b" />



sed -n -e '$p' file23
## OUTPUT
<img width="781" height="72" alt="image" src="https://github.com/user-attachments/assets/23bf170f-ccab-441c-90ff-62def98588dc" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="665" height="96" alt="image" src="https://github.com/user-attachments/assets/d79bfc03-b450-4b0a-b4a0-422248819df8" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="770" height="374" alt="image" src="https://github.com/user-attachments/assets/80bfa79c-11f9-4a6a-88d0-a4b0412be656" />
<img width="859" height="435" alt="image" src="https://github.com/user-attachments/assets/a8c5081b-be07-4bfb-806e-c1fe2858cb47" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="730" height="415" alt="image" src="https://github.com/user-attachments/assets/e96b02ef-bf3b-46d6-8312-1ac8159d3c86" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="666" height="169" alt="image" src="https://github.com/user-attachments/assets/b660d160-66e4-486a-9b41-27712779a251" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="762" height="182" alt="image" src="https://github.com/user-attachments/assets/f7ce073c-b9ba-46e5-aa65-84009804874d" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="835" height="113" alt="image" src="https://github.com/user-attachments/assets/578dd36e-290a-46fe-a8f4-538bc60ae866" />



seq 10 
## OUTPUT
<img width="779" height="273" alt="image" src="https://github.com/user-attachments/assets/11ff091c-946e-4496-9ab7-17854959ed68" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="942" height="122" alt="image" src="https://github.com/user-attachments/assets/86a5d8e6-3b72-4ef8-b8da-ba1cf72144c8" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="764" height="117" alt="image" src="https://github.com/user-attachments/assets/5ee003af-b652-4c38-b400-bfa3b397869f" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="679" height="139" alt="image" src="https://github.com/user-attachments/assets/75066f9b-a1f2-4636-996a-3e0fc1978bce" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="623" height="110" alt="image" src="https://github.com/user-attachments/assets/886ddd09-7448-42d1-81ed-d0c3a297bb40" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="839" height="119" alt="image" src="https://github.com/user-attachments/assets/6474c379-8fd0-4d1c-8c6a-76fd217de884" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="1003" height="112" alt="image" src="https://github.com/user-attachments/assets/0e821e8b-4220-473f-80ea-ba2bf71f22b3" />



sed -n '2,4{s/$/*/;p}' file23
<img width="912" height="113" alt="image" src="https://github.com/user-attachments/assets/f67f1244-a6c1-4883-bf69-4a5a335fe4fd" />


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
<img width="732" height="516" alt="image" src="https://github.com/user-attachments/assets/c6a7b102-cc10-49c7-8c63-7e14ec0144d8" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
<img width="812" height="567" alt="image" src="https://github.com/user-attachments/assets/40e3bfdc-c569-4d5c-87d1-d1cd99d716df" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="882" height="420" alt="image" src="https://github.com/user-attachments/assets/c60e92dd-ec0e-43ce-b626-d8e189fa7494" />

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="766" height="185" alt="image" src="https://github.com/user-attachments/assets/0c88ecb7-2571-45e0-80e7-907df70c5846" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="883" height="193" alt="image" src="https://github.com/user-attachments/assets/1e37a82a-85bb-41bd-8394-c5ef15799fe8" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="926" height="632" alt="image" src="https://github.com/user-attachments/assets/4578c90a-00d0-48cc-a15f-76c40a363c2f" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="989" height="632" alt="image" src="https://github.com/user-attachments/assets/3d107eb7-298e-453a-87b7-a0fd14492631" />


tar -xvf backup.tar
## OUTPUT
<img width="741" height="95" alt="image" src="https://github.com/user-attachments/assets/92dd43f4-33dd-4825-9750-a861bd19f035" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="1169" height="118" alt="image" src="https://github.com/user-attachments/assets/d8397146-9dc7-49ae-b3e7-daa9e47640c3" />

gunzip backup.tar.gz
## OUTPUT
<img width="1169" height="118" alt="image" src="https://github.com/user-attachments/assets/bed9138c-69b2-4d3f-bb10-96070f48be1d" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="872" height="233" alt="image" src="https://github.com/user-attachments/assets/ed85b97f-4390-4a13-9de9-dcd486464dcc" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="675" height="364" alt="image" src="https://github.com/user-attachments/assets/4f55f8df-9abe-4699-b3b3-e8bd4557cfd2" />


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
<img width="948" height="66" alt="image" src="https://github.com/user-attachments/assets/83263b5a-84a6-4258-9ffa-a8b6297c75b7" />

 
ls file1
## OUTPUT
<img width="915" height="772" alt="image" src="https://github.com/user-attachments/assets/277db748-b3c4-4d81-a6b8-fcd492c985c1" />

echo $?
## OUTPUT 
<img width="790" height="77" alt="image" src="https://github.com/user-attachments/assets/89a5cf8b-6ebe-4eea-9640-a7f316c3cefc" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="790" height="77" alt="image" src="https://github.com/user-attachments/assets/41c8bd29-5510-4e91-b859-447250f29160" />

abcd
 
echo $?
 ## OUTPUT
<img width="638" height="71" alt="image" src="https://github.com/user-attachments/assets/d82641a8-8762-4859-8e78-67ca4b3de5f0" />


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT
<img width="1159" height="925" alt="image" src="https://github.com/user-attachments/assets/02e60d3a-fed3-423a-b49e-010cdd63e74c" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
<img width="1160" height="746" alt="image" src="https://github.com/user-attachments/assets/ad5a4621-694d-41d0-b956-9f1a03f9ef82" />

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
<img width="1004" height="818" alt="image" src="https://github.com/user-attachments/assets/30d0e2bc-d783-4907-a047-7a7524502119" />



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
<img width="1157" height="928" alt="image" src="https://github.com/user-attachments/assets/d859d2c5-ec48-4cdd-9891-eb9948eb5c61" />

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
<img width="1149" height="930" alt="image" src="https://github.com/user-attachments/assets/965a668f-206f-4850-beb5-9fa17539e454" />

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
<img width="1160" height="928" alt="image" src="https://github.com/user-attachments/assets/7738c0f9-910a-4259-ace5-b172dd91be7f" />


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
<img width="970" height="638" alt="image" src="https://github.com/user-attachments/assets/01bdfd73-8c6c-4296-a50e-0bdf8c28a821" />

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 <img width="895" height="411" alt="image" src="https://github.com/user-attachments/assets/e9149128-c562-497f-94d2-5574d564bc6e" />

cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 <img width="884" height="545" alt="image" src="https://github.com/user-attachments/assets/df6c7a5e-ad8c-48d7-acaa-7f5fc29c221b" />

 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 <img width="884" height="545" alt="image" src="https://github.com/user-attachments/assets/379d2ebe-3479-40de-bbc7-cc4c6626b361" />

 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 <img width="771" height="812" alt="image" src="https://github.com/user-attachments/assets/40db47c0-c6ff-4909-a433-c8baf3f54578" />

 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 <img width="700" height="311" alt="image" src="https://github.com/user-attachments/assets/bf984bdb-2848-4006-9431-60e222203130" />

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 <img width="625" height="431" alt="image" src="https://github.com/user-attachments/assets/cd39728f-d398-45df-adf4-4ef28393b9fa" />

$ ./forin2.sh 
 <img width="1193" height="511" alt="image" src="https://github.com/user-attachments/assets/abdac9e6-0c61-4ffb-8915-0493d48c56e6" />

cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
<img width="727" height="286" alt="image" src="https://github.com/user-attachments/assets/ca500f3f-b088-4523-b6e9-9c491186d2d1" />

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
<img width="1193" height="511" alt="image" src="https://github.com/user-attachments/assets/839631fd-0439-43b7-b185-b7275e8d1075" />


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
<img width="727" height="286" alt="image" src="https://github.com/user-attachments/assets/38f856c8-4deb-41e3-b3a6-5c68bc968ef5" />

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
<img width="768" height="503" alt="image" src="https://github.com/user-attachments/assets/5a6937a2-581f-414d-8f51-f0b92c760ac0" />

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
<img width="731" height="362" alt="image" src="https://github.com/user-attachments/assets/4d664a5a-483e-4fff-aa16-203d77715539" />

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
<img width="658" height="386" alt="image" src="https://github.com/user-attachments/assets/b34652e5-91c8-46e9-b40a-49b1f6fcd747" />

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 <img width="440" height="226" alt="image" src="https://github.com/user-attachments/assets/02b07bd6-f0cf-4217-b5c0-8c2a0eebc994" />

cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
<img width="440" height="226" alt="image" src="https://github.com/user-attachments/assets/08005f25-3fd1-4b9b-a915-e63a0d7131da" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="440" height="226" alt="image" src="https://github.com/user-attachments/assets/5a2ba610-865d-48cc-a3be-4b85146ce0c4" />




$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
<img width="513" height="323" alt="image" src="https://github.com/user-attachments/assets/d60d3eed-75a0-4155-ac52-a8d10d274e77" />

 ./funcex.sh 

 
 ./funcex.sh 1 2
<img width="526" height="346" alt="image" src="https://github.com/user-attachments/assets/00842533-1197-4641-9c77-0095047e642f" />

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
<img width="593" height="486" alt="image" src="https://github.com/user-attachments/assets/3fae2326-9edd-42ff-8718-4f209633c813" />

<img width="569" height="322" alt="image" src="https://github.com/user-attachments/assets/99f59f8f-ecb7-4e9d-8e55-a5964df91537" />

$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 <img width="563" height="452" alt="image" src="https://github.com/user-attachments/assets/7b0afba1-a3f1-415c-ab98-e7d8610dc7e9" />

cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 <img width="563" height="452" alt="image" src="https://github.com/user-attachments/assets/a6c3acab-b31b-4bef-8403-686ee67d6231" />

 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 <img width="510" height="755" alt="image" src="https://github.com/user-attachments/assets/ced789cf-f4b2-4839-b44c-5a5d572e674a" />

cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
<img width="581" height="541" alt="image" src="https://github.com/user-attachments/assets/0c2edfff-e89e-46f5-bcc9-781a7f297cd8" />


# RESULT:
The Commands are executed successfully.
