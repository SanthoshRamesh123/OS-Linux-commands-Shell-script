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

<img width="284" height="148" alt="Screenshot 2025-10-06 131818" src="https://github.com/user-attachments/assets/43254b1d-0f1c-4e69-885c-caa5bae4f4f4" />

cat < file2
## OUTPUT


# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="287" height="177" alt="Screenshot 2025-10-06 131839" src="https://github.com/user-attachments/assets/6e6adc47-943d-4de7-9b18-35300b3df632" />

comm file1 file2
 ## OUTPUT
 
<img width="367" height="80" alt="Screenshot 2025-10-06 131859" src="https://github.com/user-attachments/assets/5cba7e20-5bf6-41cb-bd4e-07859027b8d9" />
<img width="350" height="229" alt="Screenshot 2025-10-06 131942" src="https://github.com/user-attachments/assets/2584b504-02d9-43ee-9460-065381f57df5" />

diff file1 file2
## OUTPUT

<img width="292" height="278" alt="Screenshot 2025-10-06 132005" src="https://github.com/user-attachments/assets/55b58ea0-9bea-492e-a4b0-5fbf83a28a1c" />

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

<img width="335" height="373" alt="Screenshot 2025-10-06 132249" src="https://github.com/user-attachments/assets/72377a4e-ed80-4f36-a3de-ea900298f9be" />

cut -d "|" -f 1 file22
## OUTPUT

<img width="319" height="131" alt="Screenshot 2025-10-06 132315" src="https://github.com/user-attachments/assets/e8f56ffb-d980-4cbc-a9e4-b880bf020f12" />

cut -d "|" -f 2 file22
## OUTPUT

<img width="322" height="127" alt="Screenshot 2025-10-06 132341" src="https://github.com/user-attachments/assets/11da38f8-0a93-409e-9b33-ac3978dd7466" />

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

<img width="284" height="148" alt="Screenshot 2025-10-06 131818" src="https://github.com/user-attachments/assets/d6f1f719-0300-4c50-94a3-690ad12b13aa" />

grep hello newfile 
## OUTPUT

<img width="284" height="148" alt="Screenshot 2025-10-06 131818" src="https://github.com/user-attachments/assets/9ebb04c9-f447-499c-90c3-6a338dc78139" />

grep -v hello newfile 
## OUTPUT

<img width="299" height="100" alt="Screenshot 2025-10-06 132538" src="https://github.com/user-attachments/assets/15bddbfa-19b7-4381-afbb-5466f643c074" />

cat newfile | grep -i "hello"
## OUTPUT

<img width="299" height="100" alt="Screenshot 2025-10-06 132538" src="https://github.com/user-attachments/assets/dd98dd8b-bf21-4aaf-952a-7358e713668c" />

cat newfile | grep -i -c "hello"
## OUTPUT

<img width="392" height="80" alt="Screenshot 2025-10-06 132656" src="https://github.com/user-attachments/assets/5eb37256-775d-4db3-92e7-cc6aeed45b71" />

grep -R ubuntu /etc
## OUTPUT

<img width="802" height="546" alt="Screenshot 2025-10-06 132751" src="https://github.com/user-attachments/assets/ea8d5546-9834-4cd1-83fa-f6b42a4a0f54" />

grep -w -n world newfile   
## OUTPUT

<img width="345" height="49" alt="Screenshot 2025-10-06 132832" src="https://github.com/user-attachments/assets/6b03ffe6-9a94-4888-8f67-3b028ae430b1" />

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

<img width="394" height="106" alt="Screenshot 2025-10-06 133037" src="https://github.com/user-attachments/assets/822828a9-8089-41b1-bc4b-44b0b60ae411" />

egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="355" height="103" alt="Screenshot 2025-10-06 133112" src="https://github.com/user-attachments/assets/2aef7e58-b1db-4150-9034-0ffa85567dfc" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="405" height="100" alt="Screenshot 2025-10-06 133158" src="https://github.com/user-attachments/assets/605dbfc1-80bf-4a4e-a657-ac82fb4fd4f4" />

egrep '(^hello)' newfile 
## OUTPUT

<img width="332" height="84" alt="Screenshot 2025-10-06 133226" src="https://github.com/user-attachments/assets/8ca32cd5-30ba-4c0e-831c-148a3872cf8d" />

egrep '(world$)' newfile 
## OUTPUT

<img width="322" height="99" alt="Screenshot 2025-10-06 133254" src="https://github.com/user-attachments/assets/301c019c-c118-455a-a29b-9d2f1586a27b" />

egrep '(World$)' newfile 
## OUTPUT

<img width="323" height="82" alt="Screenshot 2025-10-06 133325" src="https://github.com/user-attachments/assets/50ad1222-e410-4045-a845-e5734235f4d1" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="388" height="129" alt="Screenshot 2025-10-06 133358" src="https://github.com/user-attachments/assets/e3e423af-903c-49ff-abb1-3ce9d593b163" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="299" height="73" alt="Screenshot 2025-10-06 133426" src="https://github.com/user-attachments/assets/0c4f629a-26c4-487f-ba2c-4631d94662d1" />

egrep 'Linux.*world' newfile 
## OUTPUT

<img width="358" height="74" alt="Screenshot 2025-10-06 133452" src="https://github.com/user-attachments/assets/313b62f8-f3e5-4229-a25f-8d5d09c4c0f7" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="363" height="77" alt="Screenshot 2025-10-06 133517" src="https://github.com/user-attachments/assets/c2c28e13-1ec7-436f-8e26-7bf7ab9146b7" />

egrep l{2} newfile
## OUTPUT

<img width="403" height="122" alt="Screenshot 2025-10-06 133539" src="https://github.com/user-attachments/assets/0debb959-cc9e-43b0-8d0c-ffd86b46d5b5" />

egrep 's{1,2}' newfile
## OUTPUT 

<img width="329" height="123" alt="Screenshot 2025-10-06 133605" src="https://github.com/user-attachments/assets/1891280e-8661-44ab-a9d0-8781c052f3c8" />

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

<img width="280" height="79" alt="Screenshot 2025-10-06 133913" src="https://github.com/user-attachments/assets/141cf4d8-4a64-4679-81ee-e0c0ad4646c6" />

sed -n -e '$p' file23
## OUTPUT

<img width="286" height="73" alt="Screenshot 2025-10-06 133933" src="https://github.com/user-attachments/assets/8e51f68d-89c5-432a-9bf8-0df64447ffac" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="339" height="252" alt="Screenshot 2025-10-06 134002" src="https://github.com/user-attachments/assets/1efc68d7-766c-4b48-b1d3-52e82b402d39" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="362" height="250" alt="Screenshot 2025-10-06 134023" src="https://github.com/user-attachments/assets/daec248e-04a9-428c-be38-a694d4c8ac29" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="385" height="248" alt="Screenshot 2025-10-06 134050" src="https://github.com/user-attachments/assets/38aa93bf-c120-4ed6-9f7d-015fc4467e64" />

sed -n -e '1,5p' file23
## OUTPUT

<img width="312" height="177" alt="Screenshot 2025-10-06 134114" src="https://github.com/user-attachments/assets/3c79ec99-5882-4085-a02b-264d9a1143be" />

sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="339" height="120" alt="Screenshot 2025-10-06 134139" src="https://github.com/user-attachments/assets/bf605a26-2609-483c-a7b7-c818e76fb165" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="383" height="99" alt="Screenshot 2025-10-06 134306" src="https://github.com/user-attachments/assets/26011240-bbe4-44ac-b37d-d2de25330284" />

seq 10 
## OUTPUT

<img width="301" height="296" alt="Screenshot 2025-10-06 134318" src="https://github.com/user-attachments/assets/296c5d6a-b6cd-426d-8a1f-4015331685cf" />

seq 10 | sed -n '4,6p'
## OUTPUT

<img width="301" height="125" alt="Screenshot 2025-10-06 134343" src="https://github.com/user-attachments/assets/6e13df90-1e93-4bff-be4b-b9f6c0045877" />

seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="295" height="126" alt="Screenshot 2025-10-06 134410" src="https://github.com/user-attachments/assets/9fbeddd2-b0b6-44f7-b97b-2daa2ee0ba5f" />

seq 3 | sed '2a hello'
## OUTPUT

<img width="301" height="147" alt="Screenshot 2025-10-06 134432" src="https://github.com/user-attachments/assets/b5498045-7f25-42b3-8d18-538207871931" />

seq 2 | sed '2i hello'
## OUTPUT

<img width="306" height="125" alt="Screenshot 2025-10-06 134451" src="https://github.com/user-attachments/assets/701a3678-b98e-44ce-89ed-ef0cd833e29d" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="323" height="118" alt="Screenshot 2025-10-06 134515" src="https://github.com/user-attachments/assets/a0121847-f308-4e48-a9c4-41c73379b3a2" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="377" height="132" alt="Screenshot 2025-10-06 134550" src="https://github.com/user-attachments/assets/6931c71f-442c-44a3-ac20-d306f248b7d8" />

sed -n '2,4{s/$/*/;p}' file23

<img width="367" height="125" alt="Screenshot 2025-10-06 134649" src="https://github.com/user-attachments/assets/daeb91a3-1ba0-479d-8b05-cc730e03bed5" />

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

<img width="301" height="208" alt="Screenshot 2025-10-06 134837" src="https://github.com/user-attachments/assets/36c1b396-73a0-4214-9ced-989db60dc280" />

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

<img width="302" height="168" alt="Screenshot 2025-10-06 135027" src="https://github.com/user-attachments/assets/ecaec738-5a91-4546-8e94-59d5755fb8db" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 
<img width="419" height="253" alt="Screenshot 2025-10-06 135139" src="https://github.com/user-attachments/assets/5ceb0c42-ad40-4c99-84e0-393606778c5b" />

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

<img width="344" height="119" alt="Screenshot 2025-10-06 135332" src="https://github.com/user-attachments/assets/826602d7-b6f5-48fc-8e76-c532270512f5" />

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="425" height="129" alt="Screenshot 2025-10-06 135408" src="https://github.com/user-attachments/assets/5a386059-d701-4bda-91be-b816960685a1" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="537" height="598" alt="Screenshot 2025-10-06 135443" src="https://github.com/user-attachments/assets/ccd6752f-d13e-47c3-8c60-b945c86162d8" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="781" height="346" alt="Screenshot 2025-10-06 135546" src="https://github.com/user-attachments/assets/13c5acf1-ae85-4e3f-9a45-3ce5d5634e26" />

tar -xvf backup.tar
## OUTPUT

<img width="444" height="372" alt="Screenshot 2025-10-06 135612" src="https://github.com/user-attachments/assets/39e3b59d-6188-4554-a020-ccb8b38b0dbe" />

gzip backup.tar

ls .gz
## OUTPUT

 <img width="824" height="153" alt="Screenshot 2025-10-06 135702" src="https://github.com/user-attachments/assets/18eca608-3213-4424-b3a6-c6ebd9637056" />

gunzip backup.tar.gz
## OUTPUT

 <img width="436" height="55" alt="Screenshot 2025-10-06 135732" src="https://github.com/user-attachments/assets/68a51a92-182b-42b8-b3ad-b4684b5bc8ae" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="436" height="55" alt="Screenshot 2025-10-06 135732" src="https://github.com/user-attachments/assets/924c2fbf-78db-44b4-9668-e5f9220403cb" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="296" height="129" alt="Screenshot 2025-10-06 140235" src="https://github.com/user-attachments/assets/c0c312e6-ccda-464b-a34a-409e60c7a98e" />

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

 <img width="696" height="398" alt="Screenshot 2025-10-06 140718" src="https://github.com/user-attachments/assets/826f69a2-e9fa-4386-80b2-36bebea788ac" />

ls file1
## OUTPUT

<img width="298" height="76" alt="Screenshot 2025-10-06 140754" src="https://github.com/user-attachments/assets/fce04be3-96df-4753-8ed0-1c2c2aaef2bd" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

 <img width="624" height="147" alt="Screenshot 2025-10-06 140849" src="https://github.com/user-attachments/assets/12fb19f4-7617-4ba8-bb9e-3f2b6583a62e" />

echo $?
## OUTPUT 

 <img width="312" height="69" alt="Screenshot 2025-10-06 140807" src="https://github.com/user-attachments/assets/e0f9e91a-3465-46bb-9353-e74245ce5767" />

abcd
 
echo $?
 ## OUTPUT

<img width="336" height="150" alt="Screenshot 2025-10-06 140916" src="https://github.com/user-attachments/assets/5eae4b35-f702-497c-97b1-c9224100afd8" />

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

<img width="681" height="427" alt="Screenshot 2025-10-06 141154" src="https://github.com/user-attachments/assets/792cbdb8-b6a2-4c33-81cf-455b9d717d51" />

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

<img width="420" height="80" alt="Screenshot 2025-10-06 141422" src="https://github.com/user-attachments/assets/befd58cb-d590-4fb1-b257-a19529093c67" />

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

<img width="390" height="75" alt="Screenshot 2025-10-06 142000" src="https://github.com/user-attachments/assets/e453aa19-5c88-49ec-8e39-c57a90ed134d" />

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

<img width="742" height="134" alt="Screenshot 2025-10-06 142401" src="https://github.com/user-attachments/assets/bb8294b6-01bc-4ff5-842d-c5d6789e19dd" />

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

<img width="793" height="155" alt="Screenshot 2025-10-06 142812" src="https://github.com/user-attachments/assets/a4f8b110-1d13-4070-a102-2c50943cac27" />

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

<img width="398" height="82" alt="Screenshot 2025-10-06 143337" src="https://github.com/user-attachments/assets/450dd606-b142-48bb-ba3f-922f6298b836" />


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

<img width="760" height="413" alt="Screenshot 2025-10-06 143614" src="https://github.com/user-attachments/assets/933ce01f-0606-470b-bde5-cbc76d124fbd" />

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

 <img width="689" height="441" alt="Screenshot 2025-10-06 143944" src="https://github.com/user-attachments/assets/19275238-8577-4898-bbf6-49a96cdc3147" />

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
 
 <img width="720" height="406" alt="Screenshot 2025-10-06 150408" src="https://github.com/user-attachments/assets/74acbaeb-e383-4b40-b18d-7f25eb3e3db7" />

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
 
 <img width="645" height="506" alt="Screenshot 2025-10-06 151608" src="https://github.com/user-attachments/assets/3ada3bbb-eb08-41cc-97de-952c66861f7b" />

 
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
 
 <img width="645" height="506" alt="Screenshot 2025-10-06 151608" src="https://github.com/user-attachments/assets/417d1486-3a58-4750-a815-f6b93f3b7676" />

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

 <img width="645" height="506" alt="Screenshot 2025-10-06 151608" src="https://github.com/user-attachments/assets/ba45fdd7-7958-47f5-9355-e0898dbda998" />

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

<img width="731" height="547" alt="Screenshot 2025-10-06 151929" src="https://github.com/user-attachments/assets/4b296be9-3bd0-4fde-bf90-c5806dd9b5da" />

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

<img width="756" height="426" alt="Screenshot 2025-10-06 152146" src="https://github.com/user-attachments/assets/6bc56ba2-2642-49c2-8f25-4343551c09fa" />

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

<img width="436" height="92" alt="Screenshot 2025-10-06 152332" src="https://github.com/user-attachments/assets/40dc5e43-8da6-4d58-9186-1de3d5985835" />

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

 <img width="339" height="404" alt="Screenshot 2025-10-06 152747" src="https://github.com/user-attachments/assets/6b9eb77b-262c-438f-98e1-a1ceb22b3875" />

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

 <img width="359" height="506" alt="Screenshot 2025-10-06 153422" src="https://github.com/user-attachments/assets/dac2a1e8-8834-4ebc-8849-3816a47a7c1b" />

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

 <img width="332" height="519" alt="Screenshot 2025-10-06 154012" src="https://github.com/user-attachments/assets/b30d1c96-0e9f-4256-adf3-7893c9e1d767" />

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

<img width="425" height="324" alt="Screenshot 2025-10-06 154207" src="https://github.com/user-attachments/assets/e1fe3e95-8daa-43f6-9734-10b25acecd44" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="416" height="301" alt="Screenshot 2025-10-06 154424" src="https://github.com/user-attachments/assets/d1ef79ca-23b9-43c2-9f5b-26e5f4510065" />

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
 
<img width="586" height="498" alt="Screenshot 2025-10-06 154725" src="https://github.com/user-attachments/assets/47ddc858-4784-402c-8a5d-1d848dd60b4e" />

 
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

 <img width="577" height="504" alt="Screenshot 2025-10-06 154938" src="https://github.com/user-attachments/assets/f7180d02-2411-4fdd-b401-c27c62b911ca" />

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

 <img width="383" height="487" alt="Screenshot 2025-10-06 155339" src="https://github.com/user-attachments/assets/0d3a6c40-f7f9-4c9d-8869-78b81c98ede0" />

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
 
 <img width="418" height="627" alt="Screenshot 2025-10-06 155554" src="https://github.com/user-attachments/assets/cf55cbea-d162-45ec-bde1-d1e3db8821a4" />

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

 <img width="396" height="630" alt="Screenshot 2025-10-06 161418" src="https://github.com/user-attachments/assets/d9b5bce6-9ac3-4425-9aee-f31d9d86d2ea" />
<img width="582" height="399" alt="Screenshot 2025-10-06 161356" src="https://github.com/user-attachments/assets/4863786e-8407-49f6-96d1-d5201f9d6f09" />

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

<img width="418" height="726" alt="Screenshot 2025-10-06 161928" src="https://github.com/user-attachments/assets/968bf368-7ec3-4ec7-9448-59b90a6caa38" />

# RESULT:
The Commands are executed successfully.
