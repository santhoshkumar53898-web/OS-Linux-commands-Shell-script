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
<img width="692" height="193" alt="image" src="https://github.com/user-attachments/assets/f3cb6a9b-3bef-45d1-87e3-de424d286736" />



cat < file2
## OUTPUT
<img width="666" height="211" alt="image" src="https://github.com/user-attachments/assets/af1d7273-b45e-4b1a-a996-efbeb3d8e948" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="649" height="79" alt="image" src="https://github.com/user-attachments/assets/90347250-87aa-4a51-80e7-4635163a9e3e" />

comm file1 file2
 ## OUTPUT
<img width="561" height="196" alt="image" src="https://github.com/user-attachments/assets/d174905e-1359-45b0-950a-c304005855e1" />

 
diff file1 file2
## OUTPUT
<img width="756" height="284" alt="image" src="https://github.com/user-attachments/assets/bb236f88-9d40-4c2d-9441-9b88956c829e" />


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
<img width="565" height="117" alt="image" src="https://github.com/user-attachments/assets/dc8aad04-50ef-405d-bc4a-f53e002ec724" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="662" height="150" alt="image" src="https://github.com/user-attachments/assets/63df1eaa-b0ea-4e54-a964-aed8dc32cc94" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="565" height="145" alt="image" src="https://github.com/user-attachments/assets/0ecec305-af4d-4d20-a3ea-94e09faf457a" />


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
<img width="488" height="86" alt="image" src="https://github.com/user-attachments/assets/e4fadd89-9d74-432e-89cf-afbef252fee4" />



grep hello newfile 
## OUTPUT
<img width="558" height="81" alt="image" src="https://github.com/user-attachments/assets/a11651fc-65bd-446f-8a7a-47537fc6867a" />




grep -v hello newfile 
## OUTPUT
<img width="516" height="108" alt="image" src="https://github.com/user-attachments/assets/a9107555-e08b-443b-be71-7fc82eccca7b" />




cat newfile | grep -i "hello"
## OUTPUT
<img width="731" height="104" alt="image" src="https://github.com/user-attachments/assets/17f838d8-27a0-4a5f-b5c0-4ce82d71de88" />





cat newfile | grep -i -c "hello"
## OUTPUT
<img width="585" height="91" alt="image" src="https://github.com/user-attachments/assets/e65ae424-bcbe-4610-a495-4118f38ad4d5" />





grep -R ubuntu /etc
## OUTPUT
<img width="752" height="622" alt="image" src="https://github.com/user-attachments/assets/1bec059f-7bc7-4fdf-be7b-3b5ffa05e69d" />



grep -w -n world newfile   
## OUTPUT
<img width="613" height="104" alt="image" src="https://github.com/user-attachments/assets/217b9d07-570e-4cbd-8d61-dc4af19022fc" />


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
<img width="797" height="111" alt="image" src="https://github.com/user-attachments/assets/0b9141c3-01b8-4c3c-9974-4a218cac81d7" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="794" height="106" alt="image" src="https://github.com/user-attachments/assets/c058e410-4533-4804-a8c2-9d0a88020ddd" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="594" height="109" alt="image" src="https://github.com/user-attachments/assets/41be5aa4-124e-42c4-a6e1-78504493214e" />





egrep '(^hello)' newfile 
## OUTPUT
<img width="598" height="85" alt="image" src="https://github.com/user-attachments/assets/f8976e8c-0f27-41c1-accd-5be60ca137cd" />



egrep '(world$)' newfile 
## OUTPUT
<img width="677" height="110" alt="image" src="https://github.com/user-attachments/assets/75d527e9-d4b3-408b-9f53-bcb455fde977" />



egrep '(World$)' newfile 
## OUTPUT
<img width="464" height="85" alt="image" src="https://github.com/user-attachments/assets/a05c843d-19a0-4b51-85a7-9014a9758873" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="670" height="130" alt="image" src="https://github.com/user-attachments/assets/926abe31-bc00-40a7-83ea-e39583073ce3" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="538" height="80" alt="image" src="https://github.com/user-attachments/assets/b45eb766-d012-44ca-ab66-8937a74e8a1e" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="564" height="81" alt="image" src="https://github.com/user-attachments/assets/a2969829-181e-41c9-9992-7461a9777501" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="443" height="81" alt="image" src="https://github.com/user-attachments/assets/dc3ba416-3e33-43a2-90dc-0265181532be" />



egrep l{2} newfile
## OUTPUT
<img width="489" height="108" alt="image" src="https://github.com/user-attachments/assets/57b0c33f-45db-4851-bb2d-4596efe60f94" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="490" height="131" alt="image" src="https://github.com/user-attachments/assets/d9d8c28a-8987-443c-8ba1-127857af4d4a" />



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
<img width="751" height="87" alt="image" src="https://github.com/user-attachments/assets/ac4bd0e2-62f7-4ec0-81bd-eb6406b2d8f9" />




sed -n -e '$p' file23
## OUTPUT
<img width="688" height="79" alt="image" src="https://github.com/user-attachments/assets/815e6bfc-3cd5-4de4-b591-cdd912abe3a5" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="607" height="276" alt="image" src="https://github.com/user-attachments/assets/0d3a2d3b-686e-4479-8427-3376c2fb76eb" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="538" height="275" alt="image" src="https://github.com/user-attachments/assets/643a1711-3fb1-4cdd-94ca-8449ad5cc37a" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="590" height="273" alt="image" src="https://github.com/user-attachments/assets/2853448f-ce0b-473e-a183-37c7499c8542" />




sed -n -e '1,5p' file23
## OUTPUT

<img width="452" height="193" alt="image" src="https://github.com/user-attachments/assets/4f2f6987-daf3-493c-ba70-149c042c84a5" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="606" height="131" alt="image" src="https://github.com/user-attachments/assets/e619d5f5-f34a-4a21-af3e-826bd509a62c" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="650" height="106" alt="image" src="https://github.com/user-attachments/assets/f3bfe8a0-7d46-4727-bf13-50367135a336" />



seq 10 
## OUTPUT

<img width="688" height="315" alt="image" src="https://github.com/user-attachments/assets/c8afffa7-63c5-4224-8bdb-512f749d2005" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="513" height="130" alt="image" src="https://github.com/user-attachments/assets/e130aded-f4c4-41d0-a688-6f2edfdad4fe" />




seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="542" height="137" alt="image" src="https://github.com/user-attachments/assets/057192af-ae3a-4d0c-ab2a-f53971d6cbbb" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="511" height="155" alt="image" src="https://github.com/user-attachments/assets/c711ed3d-9fef-4bca-ae16-9d84c74b61df" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="471" height="137" alt="image" src="https://github.com/user-attachments/assets/a5ab8f50-7796-4c0c-8cd2-a9899de03877" />



seq 10 | sed '2,9c hello'
## OUTPUT
<img width="482" height="143" alt="image" src="https://github.com/user-attachments/assets/07cce0b8-30e7-4b86-a7d0-18c7d239babf" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="615" height="141" alt="image" src="https://github.com/user-attachments/assets/221f0501-91a6-44f2-a128-6956eb903fb8" />





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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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
