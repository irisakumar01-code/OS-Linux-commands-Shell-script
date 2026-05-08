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
<img width="363" height="112" alt="Screenshot 2026-04-29 170832" src="https://github.com/user-attachments/assets/62dde542-1570-40bc-9ba3-7da210e9db7b" />


cat < file2
## OUTPUT
<img width="373" height="136" alt="Screenshot 2026-04-29 170912" src="https://github.com/user-attachments/assets/b05e2079-9d9d-4481-8cf1-d4c534e70816" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="461" height="50" alt="Screenshot 2026-04-29 170943" src="https://github.com/user-attachments/assets/56acd36b-3140-404a-9db9-a93a8bd61c71" />

comm file1 file2
 ## OUTPUT
<img width="481" height="237" alt="Screenshot 2026-04-29 171035" src="https://github.com/user-attachments/assets/ee4f5ec0-595f-4ddc-ba3f-211c0ed58a27" />

 
diff file1 file2
## OUTPUT
<img width="381" height="268" alt="Screenshot 2026-04-29 171106" src="https://github.com/user-attachments/assets/7e80c958-5068-4356-ae48-c9e6b9fcb971" />


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

<img width="348" height="62" alt="Screenshot 2026-04-29 171404" src="https://github.com/user-attachments/assets/600e8563-f157-4803-8c34-54387335501a" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="440" height="92" alt="Screenshot 2026-04-29 171556" src="https://github.com/user-attachments/assets/f811cf86-84b4-46d4-9978-a1f0f5964299" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="422" height="87" alt="Screenshot 2026-04-29 171645" src="https://github.com/user-attachments/assets/12f9e481-413b-40ad-8bd2-96f248b046c5" />


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
<img width="337" height="46" alt="Screenshot 2026-04-29 171909" src="https://github.com/user-attachments/assets/88b9cbe5-9c21-4692-886e-c397adfb1a7a" />



grep hello newfile 
## OUTPUT
<img width="342" height="45" alt="Screenshot 2026-04-29 171931" src="https://github.com/user-attachments/assets/e7c32bda-37e0-4f5e-96cd-199a0e4bfa0a" />




grep -v hello newfile 
## OUTPUT
<img width="367" height="41" alt="Screenshot 2026-04-29 172006" src="https://github.com/user-attachments/assets/f314ff2c-7999-43f2-83f8-bb9341a8c373" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="466" height="70" alt="Screenshot 2026-04-29 172044" src="https://github.com/user-attachments/assets/3ec78633-e12d-452f-a19c-1193c96e0cb1" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="547" height="44" alt="Screenshot 2026-04-29 172126" src="https://github.com/user-attachments/assets/4e34a3d2-b14a-427a-bc1c-3d54c89afd6b" />



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="508" height="72" alt="Screenshot 2026-04-29 172527" src="https://github.com/user-attachments/assets/35d14406-8a58-4639-8ea2-f6b422bb66de" />


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

<img width="478" height="63" alt="Screenshot 2026-04-29 172842" src="https://github.com/user-attachments/assets/0f5198e6-81db-451d-8809-49208f321dc1" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="470" height="63" alt="Screenshot 2026-04-29 172935" src="https://github.com/user-attachments/assets/7b93e299-a2c7-4b42-9561-6bd0e53ff179" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="533" height="67" alt="Screenshot 2026-04-29 173119" src="https://github.com/user-attachments/assets/502a552a-908b-4672-b681-2bf04955bca1" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="428" height="48" alt="Screenshot 2026-04-29 173317" src="https://github.com/user-attachments/assets/7ce9825c-5c35-4dba-9752-bb5e882d86e0" />



egrep '(world$)' newfile 
## OUTPUT
<img width="419" height="91" alt="Screenshot 2026-04-29 173553" src="https://github.com/user-attachments/assets/951019cc-21ea-4dcf-ac1a-ba7b376ffcf3" />



egrep '(World$)' newfile 
## OUTPUT
<img width="419" height="91" alt="Screenshot 2026-04-29 173553" src="https://github.com/user-attachments/assets/842b487d-8e5d-4973-91b4-206f9cd0bd77" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="488" height="87" alt="Screenshot 2026-04-29 173800" src="https://github.com/user-attachments/assets/712f935c-e113-40c9-a266-f06e079bd26c" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="431" height="43" alt="Screenshot 2026-04-29 173904" src="https://github.com/user-attachments/assets/f2311fc2-0135-4f78-8365-ebaf3fb22608" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="503" height="63" alt="Screenshot 2026-04-29 174057" src="https://github.com/user-attachments/assets/7594b973-0127-4f75-a1f9-3602556e3e82" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="503" height="63" alt="Screenshot 2026-04-29 174057" src="https://github.com/user-attachments/assets/8d32b953-6f56-402f-a0e8-da7c5c2b9e55" />


egrep l{2} newfile
## OUTPUT
<img width="394" height="63" alt="Screenshot 2026-04-29 174133" src="https://github.com/user-attachments/assets/2b088be1-6413-4318-83ed-1e284b711563" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="429" height="87" alt="Screenshot 2026-04-29 174256" src="https://github.com/user-attachments/assets/e5f271ef-ac78-494e-80f5-e5d7407c1225" />


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
<img width="395" height="41" alt="Screenshot 2026-04-29 174932" src="https://github.com/user-attachments/assets/271bdac6-4de3-4711-b27b-234bb5a9b966" />



sed -n -e '$p' file23
## OUTPUT
<img width="384" height="44" alt="Screenshot 2026-04-29 175007" src="https://github.com/user-attachments/assets/3319f46c-09f7-4b56-a722-79c76cd1b201" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="482" height="197" alt="Screenshot 2026-04-29 175055" src="https://github.com/user-attachments/assets/a818b718-464f-4d3b-8aeb-bec77d1e67a8" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="510" height="195" alt="Screenshot 2026-04-29 175154" src="https://github.com/user-attachments/assets/502f6a4a-2904-49e1-b422-fb3c51780538" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="490" height="198" alt="Screenshot 2026-04-29 175235" src="https://github.com/user-attachments/assets/016e844f-7b2f-4b73-b661-9e0cd2bf43f6" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="481" height="87" alt="Screenshot 2026-04-29 175333" src="https://github.com/user-attachments/assets/210b00c5-a78a-4d13-9ae0-982eb8e6073d" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="481" height="87" alt="Screenshot 2026-04-29 175333" src="https://github.com/user-attachments/assets/db7d5a13-97fb-46d2-9a82-dcd71072e0a3" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="471" height="73" alt="Screenshot 2026-04-29 175525" src="https://github.com/user-attachments/assets/1d904f00-f068-4a8c-955d-911c8b0f6576" />


seq 10 
## OUTPUT
<img width="348" height="247" alt="Screenshot 2026-04-29 175542" src="https://github.com/user-attachments/assets/a08b7144-2bd2-46ea-b056-41b14109beaa" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="437" height="89" alt="Screenshot 2026-04-29 175620" src="https://github.com/user-attachments/assets/8c6e7fed-6797-46b9-ae0a-ece4ed9514e8" />



seq 10 | sed -n '2,~4p'
## OUTPUT



seq 3 | sed '2a hello'
## OUTPUT
<img width="414" height="109" alt="Screenshot 2026-04-29 175932" src="https://github.com/user-attachments/assets/d912d748-082c-4b72-b0e8-c24cef0f8715" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="435" height="86" alt="Screenshot 2026-04-29 180002" src="https://github.com/user-attachments/assets/93ad4c75-129b-4b44-873c-6e91231f0d16" />


seq 10 | sed '2,9c hello'
## OUTPUT


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT



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
