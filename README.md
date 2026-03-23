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

<img width="300" height="89" alt="Screenshot from 2026-01-29 13-13-46" src="https://github.com/user-attachments/assets/7a842669-33ef-4720-be39-adb029b63705" />


cat < file2
## OUTPUT
<img width="321" height="135" alt="Screenshot from 2026-01-29 13-14-03" src="https://github.com/user-attachments/assets/c5e14c20-ed37-4518-b033-fdd7e16625c3" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="362" height="44" alt="Screenshot from 2026-01-29 13-14-22" src="https://github.com/user-attachments/assets/3cf3b7e5-23fc-4109-bb0d-debeedc38d6d" />

comm file1 file2
 ## OUTPUT
<img width="375" height="198" alt="Screenshot from 2026-01-29 13-14-54" src="https://github.com/user-attachments/assets/4f137ed5-9067-43e0-a736-ebba3ce4e4b4" />

 
diff file1 file2
## OUTPUT
<img width="402" height="248" alt="Screenshot from 2026-01-29 13-15-17" src="https://github.com/user-attachments/assets/5f91eb6e-4716-437b-91f8-1a20555a6672" />


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

<img width="325" height="77" alt="Screenshot from 2026-01-29 13-34-58" src="https://github.com/user-attachments/assets/4374618a-c3a0-44de-992a-0f92499c4946" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="367" height="96" alt="Screenshot from 2026-01-29 13-36-50" src="https://github.com/user-attachments/assets/5648a932-28b1-44f8-9604-c51856e1a03d" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="371" height="95" alt="Screenshot from 2026-01-29 13-37-37" src="https://github.com/user-attachments/assets/b6b7d3ef-9ee7-4b3b-a6d9-141b12560402" />

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
<img width="365" height="50" alt="Screenshot from 2026-01-29 13-40-39" src="https://github.com/user-attachments/assets/5d89de99-d079-40e0-99ea-d921883be53f" />



grep hello newfile 
## OUTPUT
<img width="366" height="51" alt="Screenshot from 2026-01-29 13-41-59" src="https://github.com/user-attachments/assets/f5dfb606-b32c-4fb3-ac01-f13071b1ed23" />


grep -v hello newfile 
## OUTPUT
<img width="373" height="57" alt="Screenshot from 2026-01-29 13-42-38" src="https://github.com/user-attachments/assets/80b1a3ee-5efb-487b-91c3-2f6dd247888a" />

cat newfile | grep -i "hello"
## OUTPUT
<img width="471" height="72" alt="Screenshot from 2026-01-29 13-43-49" src="https://github.com/user-attachments/assets/7290a13c-a333-48f1-bd86-1f680a0e248b" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="491" height="54" alt="Screenshot from 2026-01-29 13-44-27" src="https://github.com/user-attachments/assets/5f3dbae8-2bff-42d6-b1bf-ea83cd327c3f" />



grep -R ubuntu /etc
## OUTPUT

<img width="567" height="180" alt="Screenshot from 2026-01-29 13-45-24" src="https://github.com/user-attachments/assets/c5edf19e-04d2-4219-bddd-f54450f9a4d8" />


grep -w -n world newfile   
## OUTPUT
<img width="564" height="73" alt="Screenshot from 2026-01-29 13-46-19" src="https://github.com/user-attachments/assets/624ec80d-5d25-448c-ab03-bc0f4542c3eb" />


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

<img width="533" height="79" alt="Screenshot from 2026-01-29 13-49-27" src="https://github.com/user-attachments/assets/a0e243d9-09e6-4995-a4c7-6774b1121d5c" />

egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="541" height="70" alt="Screenshot from 2026-01-29 13-50-44" src="https://github.com/user-attachments/assets/5ee249f8-da7a-4ad1-bab1-d5b08b5bc321" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="538" height="75" alt="Screenshot from 2026-01-29 13-51-38" src="https://github.com/user-attachments/assets/55ccf0da-f801-4b16-b0fc-836f91478a4c" />


egrep '(^hello)' newfile 
## OUTPUT
<img width="541" height="60" alt="Screenshot from 2026-01-29 13-52-24" src="https://github.com/user-attachments/assets/001c7bfc-de5d-4a34-b5a4-6ecfedb5d28f" />



egrep '(world$)' newfile 
## OUTPUT
<img width="541" height="54" alt="Screenshot from 2026-01-29 13-53-01" src="https://github.com/user-attachments/assets/5634be7d-5769-4326-93c1-ab413b386eb7" />



egrep '(World$)' newfile 
## OUTPUT
<img width="541" height="54" alt="Screenshot from 2026-01-29 13-53-35" src="https://github.com/user-attachments/assets/2ceb7fcb-b547-49a4-8d69-bcdd372447f1" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="543" height="75" alt="Screenshot from 2026-01-29 13-54-21" src="https://github.com/user-attachments/assets/69041d2b-33ff-4550-8783-9fe28f478e37" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="545" height="57" alt="Screenshot from 2026-01-29 13-55-20" src="https://github.com/user-attachments/assets/f5cd4013-106d-4dec-8f0b-7e9c3ba1ea8e" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="545" height="57" alt="Screenshot from 2026-01-29 13-55-54" src="https://github.com/user-attachments/assets/ae7ace61-1c2d-42c8-9b8e-fd66ae7fd3bf" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="545" height="57" alt="Screenshot from 2026-01-29 13-56-18" src="https://github.com/user-attachments/assets/102b422f-b959-4e89-a8e0-46d8c11e8493" />


egrep l{2} newfile
## OUTPUT

<img width="549" height="76" alt="Screenshot from 2026-01-29 13-56-54" src="https://github.com/user-attachments/assets/1e51afe3-5d75-4dbf-8e6a-3754ec31546e" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="545" height="97" alt="Screenshot from 2026-01-29 13-57-30" src="https://github.com/user-attachments/assets/8f30462f-36b5-41f4-8fce-00dcc0440eb5" />


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
<img width="381" height="52" alt="Screenshot from 2026-01-29 14-00-40" src="https://github.com/user-attachments/assets/0ca22540-c81d-4681-9e79-fa41ee7c0c22" />



sed -n -e '$p' file23
## OUTPUT
<img width="428" height="49" alt="Screenshot from 2026-01-29 14-01-14" src="https://github.com/user-attachments/assets/21674bb4-1ad6-4507-808b-8d88468566ca" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="424" height="200" alt="Screenshot from 2026-01-29 14-03-15" src="https://github.com/user-attachments/assets/4e4ccad9-8520-4a1d-af02-e988019215c5" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="424" height="200" alt="Screenshot from 2026-01-29 14-03-42" src="https://github.com/user-attachments/assets/4ecbf64c-e13f-4d08-af90-4ec5f0c76e27" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="469" height="203" alt="Screenshot from 2026-01-29 14-04-52" src="https://github.com/user-attachments/assets/9f882a00-09a8-4cd2-a4bf-47126f4d7331" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="470" height="139" alt="Screenshot from 2026-01-29 14-05-34" src="https://github.com/user-attachments/assets/a65f176a-ffb3-49a3-9098-69ddd4337873" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="469" height="93" alt="Screenshot from 2026-01-29 14-06-26" src="https://github.com/user-attachments/assets/88fe8156-f90d-46ee-ac68-94def482759b" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="468" height="69" alt="Screenshot from 2026-01-29 14-07-06" src="https://github.com/user-attachments/assets/35be30f6-b129-4246-a991-aeeadf22253c" />


seq 10 
## OUTPUT

<img width="470" height="241" alt="Screenshot from 2026-01-29 14-07-32" src="https://github.com/user-attachments/assets/4e704368-3286-4442-aed0-f2499e0a87b2" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="468" height="97" alt="Screenshot from 2026-01-29 14-08-06" src="https://github.com/user-attachments/assets/a6837e9e-37bf-426a-9433-bd32710d78e4" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="468" height="97" alt="Screenshot from 2026-01-29 14-08-46" src="https://github.com/user-attachments/assets/fe01ea2b-cb12-47e1-9015-73a9a4b8cbef" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="476" height="116" alt="Screenshot from 2026-01-29 14-09-59" src="https://github.com/user-attachments/assets/64fc3fbe-9b55-4a6b-9c89-82c8f06c8152" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="478" height="94" alt="Screenshot from 2026-01-29 14-10-41" src="https://github.com/user-attachments/assets/3a2f4a42-adb1-4c37-bbe0-ccdd4c17a50e" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="478" height="94" alt="Screenshot from 2026-01-29 14-11-20" src="https://github.com/user-attachments/assets/67a45437-25bb-4e6a-bee6-7e7366445861" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="478" height="94" alt="Screenshot from 2026-01-29 14-12-09" src="https://github.com/user-attachments/assets/432a010f-99e2-45bb-be33-564a2e7ec727" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="478" height="94" alt="Screenshot from 2026-01-29 14-13-44" src="https://github.com/user-attachments/assets/752d9b00-1fcc-4ffa-a225-d656749484ba" />



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
<img width="310" height="141" alt="Screenshot from 2026-01-29 14-16-41" src="https://github.com/user-attachments/assets/8dc2929d-aba6-49c3-b20b-dd83b4eec891" />


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

<img width="322" height="133" alt="Screenshot from 2026-01-29 14-19-05" src="https://github.com/user-attachments/assets/abf18b8a-226b-4d59-966e-204bd65a4799" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="565" height="200" alt="Screenshot from 2026-01-29 14-21-04" src="https://github.com/user-attachments/assets/a9aa061a-c91e-4464-824e-a8dcc942a6af" />

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
<img width="572" height="95" alt="Screenshot from 2026-01-29 14-23-37" src="https://github.com/user-attachments/assets/e5335e95-bc83-4fd8-8a57-cad84e1e380e" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="566" height="93" alt="Screenshot from 2026-01-29 14-24-36" src="https://github.com/user-attachments/assets/71b21834-d133-4db9-bac4-661a05a3e578" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="284" height="116" alt="Screenshot from 2026-01-29 14-26-04" src="https://github.com/user-attachments/assets/d8e2732a-3d53-4605-b31d-db044b5b2e46" />


tar -xvf backup.tar
## OUTPUT
<img width="393" height="140" alt="Screenshot from 2026-01-29 14-26-41" src="https://github.com/user-attachments/assets/6476d5bf-96b4-4fef-975f-a815bc055cd1" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="644" height="140" alt="Screenshot from 2026-01-29 14-28-46" src="https://github.com/user-attachments/assets/14ec6088-f822-4ba0-894b-851030369adb" />

gunzip backup.tar.gz
ls
## OUTPUT

 <img width="648" height="196" alt="Screenshot from 2026-01-29 18-44-47" src="https://github.com/user-attachments/assets/dcb39916-2663-4a54-9bd5-f752661b6ee0" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="651" height="272" alt="Screenshot from 2026-01-29 18-48-07" src="https://github.com/user-attachments/assets/640415b1-adb4-4bf6-a654-610799e5e95e" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="337" height="97" alt="Screenshot from 2026-01-29 18-38-08" src="https://github.com/user-attachments/assets/e439d2c3-ea29-4599-908d-763fcd976793" />


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
<img width="430" height="331" alt="Screenshot from 2026-01-29 18-54-42" src="https://github.com/user-attachments/assets/57d6cb51-c30d-4626-a8ef-98b0cbf5ac77" />

 
ls file1
## OUTPUT
<img width="285" height="54" alt="Screenshot from 2026-01-29 18-56-23" src="https://github.com/user-attachments/assets/f64ba6c0-df8e-4ec3-b7b9-0501342188ef" />

echo $?
## OUTPUT 

<img width="285" height="54" alt="Screenshot from 2026-01-29 18-57-06" src="https://github.com/user-attachments/assets/58ae1268-9bd3-45b6-94f7-d25cf49d48e5" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="285" height="54" alt="Screenshot from 2026-01-29 18-58-06" src="https://github.com/user-attachments/assets/4ff56ffd-1be8-45e9-8428-2e0afbd0a785" />

abcd
 
echo $?
 ## OUTPUT
<img width="469" height="221" alt="Screenshot from 2026-01-29 18-59-17" src="https://github.com/user-attachments/assets/12edac98-a0ce-4b68-801e-99d3d11b2f11" />


 
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
<img width="476" height="243" alt="Screenshot from 2026-01-29 19-02-19" src="https://github.com/user-attachments/assets/95c9250c-bec4-492e-937d-cd44ed2955f7" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="605" height="187" alt="Screenshot from 2026-01-29 19-03-22" src="https://github.com/user-attachments/assets/ae3c5fdf-a879-4a1d-8075-4d9b41bddebc" />


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
<img width="631" height="256" alt="Screenshot from 2026-01-29 19-27-20" src="https://github.com/user-attachments/assets/91c15214-1000-4aac-961b-b54394181bf5" />

check if with file location
cat>ifnested.sh
\#!/bin/bash
if[-e $HOME]
then
echo"$HOME The object exits,is it a file?"
if[-f $HOME]
then 
echo"Yes,$HOME it is a file!"
else
echo "No,$HOME it is not a file!"
if [-f$HOME/.bash_history]
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

<img width="525" height="446" alt="Screenshot from 2026-01-29 19-35-01" src="https://github.com/user-attachments/assets/98b5b838-41ce-4495-b8a6-5c226f57bca0" />


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
<img width="524" height="391" alt="Screenshot from 2026-01-29 19-38-29" src="https://github.com/user-attachments/assets/384b4e64-01ac-4364-aee6-10370de50927" />

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
<img width="573" height="471" alt="Screenshot from 2026-01-29 19-43-38" src="https://github.com/user-attachments/assets/7765c7cd-da27-4250-a4e2-71025b62e5cb" />

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
<img width="573" height="471" alt="Screenshot from 2026-01-29 19-49-43" src="https://github.com/user-attachments/assets/6518e143-1051-40c0-970a-1b6de3974e96" />


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
<img width="541" height="248" alt="Screenshot from 2026-01-29 19-52-36" src="https://github.com/user-attachments/assets/00a1d05c-7d84-4e0b-bbcc-b24e530f88c4" />

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
```bashvar
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
<img width="504" height="160" alt="Screenshot from 2026-01-29 20-43-16" src="https://github.com/user-attachments/assets/e21c742f-01cc-4439-9b7b-0164afef46e1" />

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
<img width="446" height="201" alt="Screenshot from 2026-01-29 20-14-55" src="https://github.com/user-attachments/assets/9589eb54-7543-45d4-b3ce-0befda652ac7" />


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
<img width="397" height="204" alt="Screenshot from 2026-01-29 20-17-49" src="https://github.com/user-attachments/assets/fa1449a6-0fb4-4367-88a3-d48b9ee093fa" />

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
<img width="412" height="201" alt="Screenshot from 2026-01-29 20-20-11" src="https://github.com/user-attachments/assets/837c9a3c-4c39-4e03-93a2-e05f0dadec44" />

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
<img width="753" height="287" alt="Screenshot from 2026-01-29 20-22-54" src="https://github.com/user-attachments/assets/be5ffdec-9bf7-4d05-a5e9-115d75eb85e0" />

 
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
<img width="753" height="287" alt="Screenshot from 2026-01-29 20-25-30" src="https://github.com/user-attachments/assets/bb94c090-4a85-4ac7-a9b4-ec5fe11d6aaf" />

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
 <img width="756" height="275" alt="Screenshot from 2026-01-29 20-29-14" src="https://github.com/user-attachments/assets/0633ad1a-0649-4bff-b3f9-9bb4c7cb2c17" />

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
<img width="481" height="144" alt="Screenshot from 2026-01-29 20-51-04" src="https://github.com/user-attachments/assets/f204e138-035d-4504-a224-29cebeb50c61" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="774" height="137" alt="Screenshot from 2026-01-29 20-38-08" src="https://github.com/user-attachments/assets/8ba31fda-1f7b-419e-9364-435c673fb5fd" />



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
<img width="755" height="44" alt="Screenshot from 2026-01-29 20-49-19" src="https://github.com/user-attachments/assets/0e3ad595-f92b-49be-ab27-a7182797f6fb" />

 
 ./funcex.sh 1 2
<img width="762" height="38" alt="Screenshot from 2026-01-29 20-49-58" src="https://github.com/user-attachments/assets/62e28d8d-ee3a-47c2-9ec4-7b92784fc86d" />

 
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
<img width="758" height="63" alt="Screenshot from 2026-01-29 20-48-48" src="https://github.com/user-attachments/assets/650b8e86-149e-4d29-8ea3-9526fa19113c" />

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
<img width="762" height="87" alt="Screenshot from 2026-01-29 20-48-18" src="https://github.com/user-attachments/assets/c73990eb-2931-4aae-baf2-f7b607a20981" />

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
<img width="765" height="327" alt="Screenshot from 2026-01-29 20-47-44" src="https://github.com/user-attachments/assets/c3747a0f-5eb2-4d5a-a869-c75df57db1e4" />

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
 <img width="783" height="218" alt="Screenshot from 2026-01-29 20-47-10" src="https://github.com/user-attachments/assets/0acdcd62-b7e8-4023-b20c-cf68100840c6" />

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
<img width="772" height="70" alt="Screenshot from 2026-01-29 20-46-09" src="https://github.com/user-attachments/assets/5d359561-d9b0-47f9-a53c-e356a4520bf1" />


# RESULT
The Commands are executed successfully.
