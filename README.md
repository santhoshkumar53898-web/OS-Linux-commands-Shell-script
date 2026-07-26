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
<img width="415" height="182" alt="image" src="https://github.com/user-attachments/assets/2bcf5fdd-953f-4e7a-9ee0-0553ff249028" />



cat < file2
## OUTPUT
<img width="564" height="198" alt="image" src="https://github.com/user-attachments/assets/69060a7b-667c-4006-9610-b70f91a1d88d" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="664" height="79" alt="image" src="https://github.com/user-attachments/assets/b197be99-4c4d-40cd-8034-2c064c533051" />


 
comm file1 file2
 ## OUTPUT
<img width="541" height="203" alt="image" src="https://github.com/user-attachments/assets/80fd32e1-5b0c-4b72-a8d8-c74a1f33eeff" />

 
diff file1 file2
## OUTPUT
<img width="755" height="275" alt="image" src="https://github.com/user-attachments/assets/025e8e4c-4a4b-433f-9b2a-f06ea2b85738" />



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
<img width="670" height="130" alt="image" src="https://github.com/user-attachments/assets/643f8532-d089-4ea2-8fa8-1bb0e6ad680d" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="573" height="158" alt="image" src="https://github.com/user-attachments/assets/473cd4ce-20de-45a3-acf6-da108d8a3442" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="569" height="159" alt="image" src="https://github.com/user-attachments/assets/82502317-e2ca-4fc3-8c48-7901695cabc7" />

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
<img width="577" height="69" alt="image" src="https://github.com/user-attachments/assets/ea2dbe71-b7ec-4e27-adb5-d35780041938" />



grep hello newfile 
## OUTPUT

<img width="468" height="82" alt="image" src="https://github.com/user-attachments/assets/0e52c702-bf9d-457a-85de-1522960102a1" />




grep -v hello newfile 
## OUTPUT

<img width="552" height="123" alt="image" src="https://github.com/user-attachments/assets/b80be9e3-4aa1-4e52-8e7e-d0bb53b9954c" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="572" height="107" alt="image" src="https://github.com/user-attachments/assets/ad307415-6e06-48c2-8cb2-43eef5f2057d" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="657" height="79" alt="image" src="https://github.com/user-attachments/assets/90803afe-9b6c-4f75-9c92-32d988a26cb7" />




grep -R ubuntu /etc
## OUTPUT
<img width="940" height="666" alt="image" src="https://github.com/user-attachments/assets/ec5ec4c9-830d-410c-b677-219353af7f99" />



grep -w -n world newfile   
## OUTPUT
<img width="478" height="99" alt="image" src="https://github.com/user-attachments/assets/b39edc57-0106-40da-93b3-926cd5d3e983" />



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
<img width="539" height="107" alt="image" src="https://github.com/user-attachments/assets/7f20aab5-9ce3-4c23-b5b9-e7c33251ce02" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="591" height="105" alt="image" src="https://github.com/user-attachments/assets/6f4024f2-c584-4b20-a7bb-68432a2bff38" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="524" height="106" alt="image" src="https://github.com/user-attachments/assets/c586659f-4616-485d-8de7-412806e20546" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="450" height="75" alt="image" src="https://github.com/user-attachments/assets/ddecc7f2-55fd-41cb-89b8-8a058abead48" />


egrep '(world$)' newfile 
## OUTPUT
<img width="728" height="108" alt="image" src="https://github.com/user-attachments/assets/0f2021e2-bc19-445f-80bf-709de4101a1f" />



egrep '(World$)' newfile 
## OUTPUT

<img width="547" height="83" alt="image" src="https://github.com/user-attachments/assets/b33a22ad-e4b1-4349-ad96-d7e740009187" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="732" height="127" alt="image" src="https://github.com/user-attachments/assets/55b6cac0-fdd1-4df7-9089-c5af67e0aa1f" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="706" height="73" alt="image" src="https://github.com/user-attachments/assets/9a9078a8-d102-4bff-84e5-6ab10a1c3820" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="639" height="79" alt="image" src="https://github.com/user-attachments/assets/7a2fad89-be3f-4fd0-aeb2-8bd567c24f53" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="546" height="75" alt="image" src="https://github.com/user-attachments/assets/454acd6a-5ef1-4597-98ed-558b9f87fc62" />



egrep l{2} newfile
## OUTPUT
<img width="596" height="94" alt="image" src="https://github.com/user-attachments/assets/3e6999c2-ca37-4cfc-bb6a-433a8a21f2ff" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="565" height="121" alt="image" src="https://github.com/user-attachments/assets/e5a91a73-e633-47bb-a988-5cd8be0adfb9" />


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

<img width="484" height="82" alt="image" src="https://github.com/user-attachments/assets/7b854c79-1250-4950-91f5-339979fd8895" />


sed -n -e '$p' file23
## OUTPUT
<img width="565" height="79" alt="image" src="https://github.com/user-attachments/assets/e152b7b8-8b8a-4107-a1d9-ebb4dea43ab5" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="593" height="272" alt="image" src="https://github.com/user-attachments/assets/c9561310-7a28-4731-91b6-899c1d11b5c2" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="610" height="275" alt="image" src="https://github.com/user-attachments/assets/90233087-60d8-47f8-99e3-d0ed7e855e39" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="658" height="277" alt="image" src="https://github.com/user-attachments/assets/5c77de0b-031f-4228-9931-1a7b772e54ff" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="654" height="177" alt="image" src="https://github.com/user-attachments/assets/33aadf4e-6722-4082-bdc4-b9655d225273" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="599" height="128" alt="image" src="https://github.com/user-attachments/assets/29af2c81-fc52-4536-8eb2-a6a696a20576" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="652" height="105" alt="image" src="https://github.com/user-attachments/assets/41282376-3aad-426c-9be7-ffdb63df1a96" />



seq 10 
## OUTPUT
<img width="657" height="297" alt="image" src="https://github.com/user-attachments/assets/721c4fa2-5cce-4f3e-904c-ae9a2e8f004e" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="639" height="128" alt="image" src="https://github.com/user-attachments/assets/3aff2653-c356-42e3-88fc-edcc6af36b8a" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="477" height="130" alt="image" src="https://github.com/user-attachments/assets/551a00d6-83c8-4dec-9889-8105f0f138f5" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="593" height="147" alt="image" src="https://github.com/user-attachments/assets/af1db423-d3c7-426f-be67-7dad63be3621" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="767" height="131" alt="image" src="https://github.com/user-attachments/assets/eba9c754-0ef8-4421-9e2a-70ae3d889311" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="566" height="131" alt="image" src="https://github.com/user-attachments/assets/9537e0dd-f7d3-4b95-b9d2-6fac3633e89f" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="541" height="137" alt="image" src="https://github.com/user-attachments/assets/b2c61eb9-d8d4-46a9-8ef6-26c515e19e6d" />




sed -n '2,4{s/$/*/;p}' file23


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
<img width="772" height="178" alt="image" src="https://github.com/user-attachments/assets/66fda1d3-4757-4a6e-9ef4-68ec390f23e4" />


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
<img width="606" height="154" alt="image" src="https://github.com/user-attachments/assets/adaedb3a-7159-4bc2-9931-e2529f663b36" />




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="628" height="280" alt="image" src="https://github.com/user-attachments/assets/23b5868d-1d11-4af5-b0d1-54ef6aefb6e4" />


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
<img width="689" height="126" alt="image" src="https://github.com/user-attachments/assets/fe6f9edd-d060-4dd5-b892-8afc18420678" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="680" height="136" alt="image" src="https://github.com/user-attachments/assets/f63533e7-243b-4422-9ff2-7407927ce54e" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="818" height="250" alt="image" src="https://github.com/user-attachments/assets/89d12473-d305-4a5f-95e3-d3b43d286379" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

<img width="578" height="250" alt="image" src="https://github.com/user-attachments/assets/93477341-4564-4e94-a691-3157f19c2975" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="544" height="77" alt="image" src="https://github.com/user-attachments/assets/4ccc27bd-f7b7-462c-9dc5-1af4f25bbffb" />

 
gunzip backup.tar.gz
## OUTPUT

<img width="679" height="58" alt="image" src="https://github.com/user-attachments/assets/6766e12c-ce8a-4927-9b9c-8e8d49f8305d" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="630" height="168" alt="image" src="https://github.com/user-attachments/assets/b72d43f2-7cc2-4169-b720-6c2bc3fadcea" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="615" height="129" alt="image" src="https://github.com/user-attachments/assets/4e80bc5d-b10c-4035-87aa-858a6e7591d9" />



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
 

 
./scriptest.sh 1 2 3

## OUTPUT
<img width="755" height="73" alt="image" src="https://github.com/user-attachments/assets/398c0578-5566-4986-b96a-fa2b58a9ca1e" />

 

echo $?
## OUTPUT
<img width="502" height="73" alt="image" src="https://github.com/user-attachments/assets/fbdd7a85-fd80-4bf2-b015-a0f07e870a84" />


 
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
<img width="880" height="41" alt="image" src="https://github.com/user-attachments/assets/6a63772a-dce7-4e8a-9ea2-216d377172fb" />


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
<img width="905" height="159" alt="image" src="https://github.com/user-attachments/assets/7533b70c-6783-49b2-89fa-6d9f78feff80" />



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
<img width="928" height="132" alt="image" src="https://github.com/user-attachments/assets/c0786375-c74d-4aac-ab0b-f5a5b66b7303" />


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
<img width="699" height="145" alt="image" src="https://github.com/user-attachments/assets/69772c70-7882-48d2-96e5-b28eb50cb5be" />

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
 
$ ./forin2.sh 
 
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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
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


# RESULT:
The Commands are executed successfully.
