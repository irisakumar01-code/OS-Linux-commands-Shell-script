
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

<img width="432" height="88" alt="Screenshot 2026-05-19 095724" src="https://github.com/user-attachments/assets/b3255a23-9a25-4655-a302-248f2b644d36" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="414" height="109" alt="Screenshot 2026-04-29 175932" src="https://github.com/user-attachments/assets/d912d748-082c-4b72-b0e8-c24cef0f8715" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="435" height="86" alt="Screenshot 2026-04-29 180002" src="https://github.com/user-attachments/assets/93ad4c75-129b-4b44-873c-6e91231f0d16" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="432" height="88" alt="Screenshot 2026-05-19 095724" src="https://github.com/user-attachments/assets/adc703b2-38d9-4e79-97f3-a9c73c5eff1c" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="591" height="87" alt="Screenshot 2026-05-19 095815" src="https://github.com/user-attachments/assets/730cba3d-68dd-4cbb-8a9c-e768ca8540a9" />


sed -n '2,4{s/$/*/;p}' file23
<img width="506" height="87" alt="Screenshot 2026-05-19 095826" src="https://github.com/user-attachments/assets/c48da0e9-cc91-4dbe-9800-d90b6f840d89" />


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
<img width="342" height="128" alt="Screenshot 2026-05-19 100109" src="https://github.com/user-attachments/assets/8c5d4870-5726-48a0-b419-14141c8f11bb" />


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

<img width="327" height="127" alt="Screenshot 2026-05-19 100222" src="https://github.com/user-attachments/assets/fb12a382-77d8-4ba0-bc62-e85e4ce711f5" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="581" height="196" alt="Screenshot 2026-05-19 100324" src="https://github.com/user-attachments/assets/146dc1b1-7470-4646-85c4-48b846cfe151" />


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
<img width="488" height="92" alt="Screenshot 2026-05-19 100446" src="https://github.com/user-attachments/assets/94a97225-9237-473a-b01b-66c73957e7e8" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="625" height="82" alt="Screenshot 2026-05-19 100514" src="https://github.com/user-attachments/assets/3d139603-39c9-4a10-8158-ed238a9f0972" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="450" height="197" alt="Screenshot 2026-05-19 100609" src="https://github.com/user-attachments/assets/70629588-00c3-4abf-8e7d-de43d8ddee37" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="768" height="192" alt="Screenshot 2026-05-19 100732" src="https://github.com/user-attachments/assets/aef8952e-4c43-4c34-a204-0a4d7ab19f86" />


tar -xvf backup.tar
## OUTPUT
<img width="768" height="192" alt="Screenshot 2026-05-19 100732" src="https://github.com/user-attachments/assets/c53848a8-9ab2-4084-b703-372542d8ec8f" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="447" height="83" alt="Screenshot 2026-05-19 100834" src="https://github.com/user-attachments/assets/cc90b3bc-5d37-4f37-8ad3-cae5ca5586ee" />

gunzip backup.tar.gz
## OUTPUT
<img width="740" height="67" alt="Screenshot 2026-05-19 101220" src="https://github.com/user-attachments/assets/30c6668d-7dca-40bb-8e23-327cc6fb11e1" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="740" height="67" alt="Screenshot 2026-05-19 101220" src="https://github.com/user-attachments/assets/3bc3b869-07e4-4ca6-8ddc-70d2347b19e9" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="432" height="85" alt="Screenshot 2026-05-19 101526" src="https://github.com/user-attachments/assets/84875b95-04c6-4656-a1c7-57256141a998" />


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
<img width="667" height="631" alt="Screenshot 2026-05-19 101804" src="https://github.com/user-attachments/assets/8e0d086b-3f2b-4773-9a02-201697cc20ac" />

 
ls file1
## OUTPUT
<img width="405" height="70" alt="Screenshot 2026-05-19 102102" src="https://github.com/user-attachments/assets/15d1b63e-7847-4b9b-9c4d-bf6885dfc025" />

echo $?
## OUTPUT 
<img width="405" height="70" alt="Screenshot 2026-05-19 102102" src="https://github.com/user-attachments/assets/ac3af9b0-8417-4382-ba0a-37be7f62d694" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="332" height="38" alt="Screenshot 2026-05-19 102146" src="https://github.com/user-attachments/assets/ee083df4-d96b-43f7-ac7d-561f88da1134" />

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

<img width="362" height="25" alt="Screenshot 2026-05-19 102411" src="https://github.com/user-attachments/assets/9588b3f8-eb58-4827-8e63-c7dbe763d0ad" />


chmod 755 strcomp.sh
 
./strcomp.sh 



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
<img width="452" height="17" alt="Screenshot 2026-05-19 102553" src="https://github.com/user-attachments/assets/3a963d6b-0a4d-4ef3-ab21-1f1915dbd2cd" />

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
<img width="461" height="106" alt="Screenshot 2026-05-19 102849" src="https://github.com/user-attachments/assets/54c7cc3f-fba6-4ed8-b9c6-71c4bde211d5" />

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
<img width="455" height="412" alt="Screenshot 2026-05-19 103024" src="https://github.com/user-attachments/assets/7c6cea91-8d2a-4b8b-a743-cef622f9d398" />


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
<img width="387" height="108" alt="Screenshot 2026-05-19 103258" src="https://github.com/user-attachments/assets/6b6b21e2-1439-4e18-9b43-24775713f3b4" />


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
<img width="455" height="30" alt="Screenshot 2026-05-19 103438" src="https://github.com/user-attachments/assets/8813ec19-0a7d-4991-a593-2519b972a4d0" />

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
output:
<img width="478" height="65" alt="Screenshot 2026-05-19 103546" src="https://github.com/user-attachments/assets/d1ed2d0c-301f-4b49-9bf4-ca6a2a14c5b3" />

 
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
 
 output:
 <img width="502" height="261" alt="Screenshot 2026-05-19 103849" src="https://github.com/user-attachments/assets/349a10ee-bda6-462d-9395-5901478af4ab" />

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
output:
<img width="488" height="135" alt="Screenshot 2026-05-19 104000" src="https://github.com/user-attachments/assets/1e154c77-a364-4b2d-a3c0-79049b59a8a5" />

 
 
 
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
 output:
 <img width="455" height="168" alt="Screenshot 2026-05-19 104144" src="https://github.com/user-attachments/assets/e3a0bd8a-296a-4062-a2bf-181108af2407" />

 
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
 output:
 <img width="476" height="107" alt="Screenshot 2026-05-19 104233" src="https://github.com/user-attachments/assets/30ffbea5-390d-47dc-b4df-51c7c001c366" />

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
 output:
 <img width="476" height="107" alt="Screenshot 2026-05-19 104233" src="https://github.com/user-attachments/assets/34670640-a482-4e63-a144-e7913ec6b753" />

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
output:
<img width="475" height="177" alt="Screenshot 2026-05-19 104322" src="https://github.com/user-attachments/assets/d60e2d8f-5453-4021-94c4-14f8ecd768e4" />

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
output:
<img width="503" height="202" alt="Screenshot 2026-05-19 104536" src="https://github.com/user-attachments/assets/20faf6a8-9ee4-4b78-be8d-3808b6210ecf" />

$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam


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
<img width="483" height="147" alt="Screenshot 2026-05-19 104646" src="https://github.com/user-attachments/assets/6614320d-e2e6-4e59-a4e7-9ffd3b9fcdaa" />

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
<img width="613" height="153" alt="Screenshot 2026-05-19 104756" src="https://github.com/user-attachments/assets/c98c5d0e-3b92-44f8-94fe-4dfc41b5754b" />

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
<img width="487" height="307" alt="Screenshot 2026-05-19 104836" src="https://github.com/user-attachments/assets/9faaa5df-4787-4f86-b9a8-5feab97677d0" />

 
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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
output:
<img width="497" height="116" alt="Screenshot 2026-05-19 104921" src="https://github.com/user-attachments/assets/4524aa7a-f5a4-4a92-b77b-eab1d16e8b04" />

 
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
 <img width="516" height="155" alt="Screenshot 2026-05-19 105025" src="https://github.com/user-attachments/assets/cf6950c4-309f-49d3-924d-dc863a23cb15" />

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
<img width="595" height="90" alt="Screenshot 2026-05-19 105115" src="https://github.com/user-attachments/assets/4b28c21d-af0f-4983-854f-87548c8efe06" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh
## OUTPUT
<img width="517" height="87" alt="Screenshot 2026-05-19 105232" src="https://github.com/user-attachments/assets/0ca3faba-fac6-4634-b158-997f99d0c052" />

 
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
<img width="398" height="41" alt="Screenshot 2026-05-19 105404" src="https://github.com/user-attachments/assets/05c643d8-960f-45b8-9ac5-1a7f535f4318" />

 
 ./funcex.sh 1 2
<img width="460" height="35" alt="Screenshot 2026-05-19 105412" src="https://github.com/user-attachments/assets/a76fbde4-fcf4-488e-ae45-61728052a833" />

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
## OUTPUT
$ chmod 777 argshift.sh

$ ./argshift.sh 1 2 3
<img width="495" height="107" alt="Screenshot 2026-05-19 105534" src="https://github.com/user-attachments/assets/bf695677-3012-4e9c-b5df-ee4433ba9ca7" />

 
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

$ ./argshift.sh 1 2 3
 ## OUTPUT
 <img width="560" height="120" alt="Screenshot 2026-05-19 105622" src="https://github.com/user-attachments/assets/127ddf70-20a2-4fff-b3fb-249ad27dbf26" />

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
 <img width="637" height="596" alt="Screenshot 2026-05-19 105706" src="https://github.com/user-attachments/assets/3fdd3721-17b9-482d-824a-3220579b13e0" />

 
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
<img width="511" height="307" alt="Screenshot 2026-05-19 105840" src="https://github.com/user-attachments/assets/31d97a6e-d61f-47bb-bbd1-8ec5648e7536" />
 
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
<img width="500" height="117" alt="Screenshot 2026-05-19 105927" src="https://github.com/user-attachments/assets/ac8326e0-0126-466b-9d28-3fcbe67e9eaa" />


# RESULT:
The Commands are executed successfully.
