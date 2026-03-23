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
<img width="450" height="148" alt="545136784-76018746-5d2f-4356-b21c-52880ff3b8d2" src="https://github.com/user-attachments/assets/0b1cb7dd-42f9-4963-96c8-51f23040405b" />



cat < file2
## OUTPUT

<img width="420" height="203" alt="545137827-d5614c93-365f-4ab2-b912-ce68639a3f8e" src="https://github.com/user-attachments/assets/d6ed028b-72ac-43b0-9ffc-4df3eb129338" />

# Comparing Files
cmp file1 file2
## OUTPUT
<img width="420" height="203" alt="545137827-d5614c93-365f-4ab2-b912-ce68639a3f8e" src="https://github.com/user-attachments/assets/740e8432-76e7-4062-b17a-c50f11328e6b" />
 
comm file1 file2
 ## OUTPUT
<img width="521" height="58" alt="545138110-10f8ca6b-47d0-462f-bb87-44508bb29247" src="https://github.com/user-attachments/assets/6b4e0211-c4d3-42ef-b9d9-f832d69cd30c" />

 
diff file1 file2
## OUTPUT
<img width="534" height="385" alt="545138464-3a834144-4208-4bc3-a23c-c2c28266354e" src="https://github.com/user-attachments/assets/bc51a3be-9d08-4c1c-807f-72a38c1c50ab" />


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

<img width="478" height="114" alt="545139075-276f0bfb-34b6-41c8-9c54-023c599d9186" src="https://github.com/user-attachments/assets/34a8ff1e-f3ce-440f-bf49-0e07b34394d1" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="544" height="140" alt="545139274-285bb92f-9991-4d01-9f0d-cc5b5c760f9e" src="https://github.com/user-attachments/assets/109eb890-e4ea-4aa9-9db9-0a639e9593b6" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="543" height="134" alt="545139442-f3d468cd-3fc7-411c-94df-6e8bb475da65" src="https://github.com/user-attachments/assets/ffa8af2f-d6e1-465f-b474-103fa77be0b0" />

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

<img width="521" height="63" alt="545139730-14e7faab-e92c-4f26-8ffd-c4dab9313e31" src="https://github.com/user-attachments/assets/c285bccc-c33f-40c9-b99f-985aff4d17d1" />


grep hello newfile 
## OUTPUT

<img width="489" height="79" alt="545140006-965564ac-37c5-4ed7-a49d-6f02d781ea8f" src="https://github.com/user-attachments/assets/b54d40c4-bbb4-4624-9645-d81bc5217087" />



grep -v hello newfile 
## OUTPUT

<img width="538" height="78" alt="545140191-0009b0c0-8b80-41ab-8cb0-b29289ac9e1d" src="https://github.com/user-attachments/assets/0a25a9bb-b8b5-4641-a8da-7934a24df0b7" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="686" height="95" alt="545140354-9a8ce86d-7f70-40e7-9296-7b4d8f797421" src="https://github.com/user-attachments/assets/26cf35d6-218e-48fa-b000-9519648af087" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="732" height="65" alt="545140574-e8cfaecd-fc2b-4aac-8087-668645cf2e82" src="https://github.com/user-attachments/assets/23798e82-5621-400b-b618-9dadba950022" />


grep -R ubuntu /etc
## OUTPUT


<img width="764" height="268" alt="545140850-9b08b96c-1040-41f0-91d7-851bbba04262" src="https://github.com/user-attachments/assets/5eda67df-d2d5-4f30-ac71-45cec4f0353d" />

grep -w -n world newfile   
## OUTPUT

<img width="593" height="105" alt="545141104-09ba8e48-e77e-4fda-bb92-73c687625f2e" src="https://github.com/user-attachments/assets/f78c89b3-0257-4894-95a8-eefe8329fabf" />

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

<img width="710" height="103" alt="545141298-9fcac5af-08ff-48e9-98aa-f3017d605bcd" src="https://github.com/user-attachments/assets/f00140c5-2872-46e0-95d5-276e00840ba5" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="650" height="106" alt="545141474-d6ce9c77-ed04-4f55-a46f-18a0a0518b7b" src="https://github.com/user-attachments/assets/dd0f66cc-ef8a-436f-86c7-dd9cc0583ef7" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="758" height="106" alt="545141654-20a2cd3b-bae4-4ab7-b846-6c9973ce4c26" src="https://github.com/user-attachments/assets/f58b34c0-a741-4c5c-9f88-e427626ecf32" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="615" height="75" alt="545141989-a5090601-f6c4-4fc1-af6a-d402fd6d7cd1" src="https://github.com/user-attachments/assets/e36cec42-90bc-42be-a193-d528f0361316" />


egrep '(world$)' newfile 
## OUTPUT
<img width="609" height="78" alt="545142157-8838f067-c4f8-49a4-9b78-eeb2ac3653df" src="https://github.com/user-attachments/assets/87d5c9d7-20cf-46f0-a562-1d0ca32f30c3" />



egrep '(World$)' newfile 
## OUTPUT
<img width="603" height="61" alt="545142363-0545d732-ca75-489f-ac6c-0de4a9eafccc" src="https://github.com/user-attachments/assets/f0ae1ba0-ff81-4d70-984e-45226958c74c" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="696" height="95" alt="545142562-8eb3b919-31b0-4b57-9780-5d05833f2c43" src="https://github.com/user-attachments/assets/ec0f89fa-e8ab-42b6-b53b-11082b0134c3" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="592" height="67" alt="545142757-037aa347-897c-475e-8664-24925c7e7800" src="https://github.com/user-attachments/assets/45590e20-5465-43f1-a01c-e4781295244c" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="682" height="71" alt="545142878-278ee247-ca8a-47ee-be8e-48c51165ad24" src="https://github.com/user-attachments/assets/43e29fef-d9b0-49c2-8d8c-b15153337eae" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="675" height="67" alt="545143088-17496cec-9392-4150-a111-727f3a52b631" src="https://github.com/user-attachments/assets/a7559a59-d3ed-4330-b3dc-7509b0341ae0" />


egrep l{2} newfile
## OUTPUT
<img width="610" height="108" alt="545143295-549f2488-91e3-40ad-b7a1-026824d48ed9" src="https://github.com/user-attachments/assets/30528460-5ba0-4531-bac9-d832d000cc16" />



egrep 's{1,2}' newfile
## OUTPUT 

<img width="606" height="146" alt="545143462-13100856-a21e-4bfe-8b34-b6845c20bb5a" src="https://github.com/user-attachments/assets/2975dc02-334e-4624-b663-60200ea97300" />

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

<img width="564" height="60" alt="545144242-1f066474-2aba-44a4-867a-536135ac90a2" src="https://github.com/user-attachments/assets/a067149e-0857-4505-9d71-d6c97a497f62" />


sed -n -e '$p' file23
## OUTPUT
<img width="573" height="64" alt="545144415-a516d0b5-857f-40bb-a9e1-2944c8f67331" src="https://github.com/user-attachments/assets/d999e898-3b14-407b-a92b-bb125e92865d" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="651" height="304" alt="545144634-d8032195-b743-4564-8a80-9edf494f6b99" src="https://github.com/user-attachments/assets/e972acd6-850d-449e-8845-1e310f0966a6" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="650" height="303" alt="545144807-03752638-4e5a-45c0-bac8-4dcff6d5a114" src="https://github.com/user-attachments/assets/80d4938a-e1df-4792-a82e-acf33a084a53" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="683" height="311" alt="545144997-93a1ad0d-dc00-4629-93c7-1745a74ec6ae" src="https://github.com/user-attachments/assets/a08870e0-c081-4580-8938-1a08b2acf21b" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="593" height="207" alt="545145185-d62b78a3-b616-4174-a6f3-c93855ebf677" src="https://github.com/user-attachments/assets/c0a9a90b-fb43-49bd-b616-20af6ace8b6b" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="648" height="142" alt="545145350-9b057bae-a041-4f13-b4e5-43fbd7da36e0" src="https://github.com/user-attachments/assets/391379cd-03d1-4244-b7aa-d657303526e7" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="696" height="101" alt="545145660-ea8a4da3-2e7e-4f59-8e2c-9fafb5f6d0fb" src="https://github.com/user-attachments/assets/1e03d43c-6c78-4237-9ea8-5799c7e0ba7b" />


seq 10 
## OUTPUT

<img width="418" height="370" alt="545146067-23863d1f-d56e-4792-bcec-aa1f7dc3f1dc" src="https://github.com/user-attachments/assets/708b15e9-065d-4a03-91c8-5dc1cae7e1ed" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="613" height="141" alt="545146482-771b3428-f113-4fdf-9b5a-0a853023fc2c" src="https://github.com/user-attachments/assets/b44a41ad-4aa1-4865-9561-7ddebfef3a67" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="640" height="130" alt="545146952-d47659a3-2327-4ec4-bd75-be26d9416843" src="https://github.com/user-attachments/assets/e7a17470-784d-4745-92ce-e47e323d31e9" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="593" height="167" alt="545146953-b955c606-45cd-46a8-9cd4-fa473e09660f" src="https://github.com/user-attachments/assets/26b4496c-f101-459b-866f-4a5a5e07e8b1" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="574" height="137" alt="545147106-e44dfdfa-5e6b-40ce-8039-2b4b677cd9e4" src="https://github.com/user-attachments/assets/ed551c41-a5e4-49ca-ab03-232b0dfc2623" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="625" height="134" alt="545147306-8eaff76c-6e9e-44be-bd19-4c77f3ff97b0" src="https://github.com/user-attachments/assets/9b5f0c3e-23e2-4477-a4ce-24d0fd6e51c5" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="679" height="137" alt="545147506-cd99a78d-22f0-4adf-a1dc-3bf31ca5a9fc" src="https://github.com/user-attachments/assets/1158e911-a944-40c4-87cf-6035332139a6" />


sed -n '2,4{s/$/*/;p}' file23
<img width="713" height="141" alt="545147795-6812c93d-d1cf-4225-846b-206d8a4f4a26" src="https://github.com/user-attachments/assets/c1136458-b114-43c0-ad71-7dd977a42b48" />


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
<img width="433" height="203" alt="545148099-647e1d06-2046-4046-8dc9-95426378714f" src="https://github.com/user-attachments/assets/6eec5517-03e5-47a5-aeb6-2d2dc8596908" />


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
<img width="453" height="201" alt="545148270-4dc061ab-6a5c-4de9-b698-41dcf867597d" src="https://github.com/user-attachments/assets/04b8dce7-3422-4806-9dc7-ad2a642c84f3" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="790" height="289" alt="545148430-a49e0eb8-3c2b-44d9-8d81-eb20948b7d6b" src="https://github.com/user-attachments/assets/5258ac10-66c5-45c2-9688-bdc7e263a988" />

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
<img width="536" height="113" alt="545149504-d9148edc-8d85-45cf-8b0c-553938a6c1fd" src="https://github.com/user-attachments/assets/8190f958-4ba3-4b7b-b2bb-21e77b4bbda9" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="664" height="109" alt="545149818-9de68229-c05b-41f7-b24e-a63887754cad" src="https://github.com/user-attachments/assets/91121d06-78aa-4109-ae59-bc0304d9f717" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="304" height="149" alt="545151024-8779ba7c-7d97-424a-9a53-9e9a343d78b2" src="https://github.com/user-attachments/assets/678dabdb-6f69-44e7-8f5f-a1db9e4257e9" />


tar -xvf backup.tar
## OUTPUT
<img width="474" height="163" alt="545151092-41047c7f-3eec-40f9-8e54-c817a738e3f1" src="https://github.com/user-attachments/assets/6872ec57-1073-4251-a521-aee35bb46f28" />

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT
<img width="784" height="162" alt="545151474-09d5dc96-1326-4f48-8545-f414d47d386d" src="https://github.com/user-attachments/assets/27dc39f4-e9cb-4615-b2ed-ecb9fe2ae3e8" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="785" height="335" alt="545151720-d577e5ad-f514-4c66-a60f-efb308ac5d61" src="https://github.com/user-attachments/assets/66e5d1dc-d12e-43f3-900c-c462bb24ebac" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="396" height="109" alt="545151799-97dec981-9957-4c8c-a54b-8814b9a5e05e" src="https://github.com/user-attachments/assets/846b0988-e2a4-4898-a107-f3a22009c126" />

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
<img width="454" height="411" alt="545151916-80beb979-0396-4a95-a153-f827770c2a66" src="https://github.com/user-attachments/assets/6ea9551a-28f2-49b9-83d7-55fae67e4bfd" />

 
ls file1
## OUTPUT
<img width="274" height="55" alt="545152267-b8334bbb-a25e-495e-8820-99b77384696d" src="https://github.com/user-attachments/assets/e9f99ce5-c7cc-4625-bbd5-d96ce89f1817" />

echo $?
## OUTPUT 
<img width="290" height="56" alt="545152364-cbf8fea3-1be0-45f2-be48-98739afebce2" src="https://github.com/user-attachments/assets/9caf54b3-9396-4d63-a352-8c8339b7b00f" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="265" height="64" alt="545152863-4c2b8c61-0f4d-4daf-8cc6-6fe29c78048d" src="https://github.com/user-attachments/assets/c0069f7b-1d07-4f1c-962c-64bb78efc865" />

abcd
 
echo $?
 ## OUTPUT
<img width="557" height="268" alt="545153029-48d4f3eb-8a95-4133-8191-97de50beca64" src="https://github.com/user-attachments/assets/a91a20a0-74e1-414d-bac4-90bbb4cb7d30" />


 
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

<img width="542" height="299" alt="545153315-1df8ad43-621e-4571-be68-7cf6ffcf0c61" src="https://github.com/user-attachments/assets/bbf89d10-4b39-4f66-b4c5-3bdb6a13762f" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="725" height="222" alt="545153622-bc91cb4e-0141-4bd3-8b6f-d44d8b2645fd" src="https://github.com/user-attachments/assets/ee2c134f-78c9-4bc1-8c44-fc3d23cf6e6c" />


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
<img width="751" height="307" alt="545153725-fb5787d0-0fad-4cc5-a6ee-e2a2d3b07cd5" src="https://github.com/user-attachments/assets/f193fd2e-3ade-4538-be48-21780512c4bd" />

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

<img width="605" height="583" alt="545154011-48c87faa-bcfc-4cb1-b613-82b5a98299a6" src="https://github.com/user-attachments/assets/aea52179-00f8-4384-bf4e-fa3e15704124" />


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
<img width="579" height="473" alt="545154457-aab75f99-924d-4bee-9b45-cd9536e043a0" src="https://github.com/user-attachments/assets/a373d5ab-3011-4c59-b9d8-94064fee727f" />

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
<img width="587" height="582" alt="545155536-8c8036a6-45b4-47dc-bbab-2eabef09512e" src="https://github.com/user-attachments/assets/9ae84025-b2a1-4fc5-b467-86eb001a009f" />

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
<img width="690" height="571" alt="545155733-47499a2f-ff4c-4c63-ab60-5fe58fe96fe7" src="https://github.com/user-attachments/assets/0a43df85-d79e-46db-b69a-bbadbb28d58a" />


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
<img width="584" height="298" alt="545155846-b92f1268-0338-440b-a02c-5b8ac29e9b2d" src="https://github.com/user-attachments/assets/f008dbec-f343-4f66-9b6d-e26903f0508d" />

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
https://github.com/user-attachments/assets/5d295aff-e4b-4975-b2da-3e97290c3c9e
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
<img width="452" height="246" alt="545159111-0aa8df00-f9cb-4ffa-997e-c41b81c1ff5d" src="https://github.com/user-attachments/assets/13dd6719-3c66-453d-8f33-cc243974983c" />



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
<img width="461" height="243" alt="545159199-f6e9f4e9-5e75-4e53-b28d-a88d868d1fd0" src="https://github.com/user-attachments/assets/4a8cdef5-6746-44fe-bba6-ab28d13ac515" />

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
<img width="448" height="243" alt="545159369-3704b69f-3260-4902-9d90-7395fdee7dfc" src="https://github.com/user-attachments/assets/c0ca1795-e050-4fdd-a4ed-ce3ffd9dffc1" />

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
<img width="782" height="309" alt="545159465-5fc1adf7-a383-456d-94e1-1706f819df09" src="https://github.com/user-attachments/assets/7d0f472c-4f45-4df9-99ff-7770c33a9095" />

 
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
<img width="791" height="305" alt="545159784-0b39075c-ee70-4336-9732-297a7409cbeb" src="https://github.com/user-attachments/assets/b3a88a41-0ebb-4cd3-a301-318ec292f45b" />

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
 <img width="517" height="282" alt="545159849-ae0d7a24-8c4e-4f9b-ac68-8128de508a1d" src="https://github.com/user-attachments/assets/aca3349a-ce09-41bb-a310-1412bba8c4b3" />

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
<img width="526" height="172" alt="545160147-1492f761-996a-4e1f-b52a-b7c79ad93057" src="https://github.com/user-attachments/assets/252e0290-b8f2-481c-b330-3775bc1ef6cb" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="471" height="135" alt="545160188-816b1542-13ff-44b6-8aff-60d66f977eb4" src="https://github.com/user-attachments/assets/14971516-b285-4678-86f8-a3fd14f985be" />



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
 ./funcex.sh <img width="336" height="39" alt="545160302-f13ac471-8600-45ed-bb53-6510f3a7dfbf" src="https://github.com/user-attachments/assets/e4ba1b55-c885-4a0b-b4aa-08984b6040e4" />


 
 ./funcex.sh 1 2<img width="313" height="35" alt="545160327-27498716-0b04-4a8c-9f08-352861a208a3" src="https://github.com/user-attachments/assets/e94fe914-49f9-4822-8543-1bba41413741" />


 
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
<img width="373" height="59" alt="545160390-d0880540-0465-4316-982f-e3a10bb734c0" src="https://github.com/user-attachments/assets/f40e554f-fe80-4c39-b185-7d72c9590f58" />

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
<img width="338" height="87" alt="545160493-ae4dfe31-3af4-48ae-869e-57c00c4bd5d6" src="https://github.com/user-attachments/assets/a40b86f7-0f9b-45d0-93e7-c87744bd4b43" />

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
<img width="310" height="335" alt="545160641-3f66b74c-8186-4b4c-a588-896fa6ac2cb9" src="https://github.com/user-attachments/assets/4ad56d05-2e2a-4be0-9e25-c9f68fcd000f" />
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
 <img width="298" height="225" alt="545160845-a5d3c3a9-9fc4-40ba-9e9a-3541fc79172e" src="https://github.com/user-attachments/assets/5db07877-a33f-43e6-aeb1-e36ff63b90ba" />

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
<img width="772" height="63" alt="545161053-0837a29b-ddb2-46b4-8cb1-0f4d3a8f31b2" src="https://github.com/user-attachments/assets/a3dab00f-a21a-41eb-99fa-3e465c4bb976" />


# RESULT:
The Commands are executed successfully.
