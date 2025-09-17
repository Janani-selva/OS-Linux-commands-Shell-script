 /># OS-Linux-commands-Shell-scripting
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

<img width="485" height="118" alt="Screenshot from 2025-09-18 02-57-50" src="https://github.com/user-attachments/assets/f61ddced-bcc6-418a-9884-8b321c49e9cc" />


cat < file2
## OUTPUT
<img width="485" height="131" alt="Screenshot from 2025-09-18 02-59-04" src="https://github.com/user-attachments/assets/eb480f7f-e90b-4049-bb8f-4f4fe1d29a96" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="481" height="42" alt="Screenshot from 2025-09-18 02-59-22" src="https://github.com/user-attachments/assets/8be5ac6d-2450-41c1-85fc-4ef6d0064e16" />

comm file1 file2
 ## OUTPUT
<img width="459" height="240" alt="Screenshot from 2025-09-18 02-59-44" src="https://github.com/user-attachments/assets/cb4052e1-2400-49c6-bb18-05ed0474cc0a" />

 
diff file1 file2
## OUTPUT
<img width="451" height="188" alt="Screenshot from 2025-09-18 03-00-04" src="https://github.com/user-attachments/assets/2f97c78b-662a-4b1b-a019-65dbf7958c36" />


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
<img width="424" height="78" alt="Screenshot from 2025-09-18 03-02-44" src="https://github.com/user-attachments/assets/e2f0f884-2896-40ac-8e4f-28cd2a3ad006" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="422" height="97" alt="Screenshot from 2025-09-18 03-03-11" src="https://github.com/user-attachments/assets/dd352975-afeb-4e22-ad13-e042d2e2ebc1" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="422" height="97" alt="Screenshot from 2025-09-18 03-03-32" src="https://github.com/user-attachments/assets/44dc43e4-54f8-4294-8012-9aad14b4360d" />


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
<img width="420" height="45" alt="Screenshot from 2025-09-18 03-04-26" src="https://github.com/user-attachments/assets/e69ea149-227f-467f-b830-32a3ca131505" />



grep hello newfile 
## OUTPUT

<img width="420" height="45" alt="Screenshot from 2025-09-18 03-04-41" src="https://github.com/user-attachments/assets/ccb8d15a-8bb2-427e-8cde-aa5dd9f49fcf" />



grep -v hello newfile 
## OUTPUT
<img width="420" height="45" alt="Screenshot from 2025-09-18 03-04-55" src="https://github.com/user-attachments/assets/32788411-c49e-4614-af96-dc689f4b0108" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="514" height="46" alt="Screenshot from 2025-09-18 03-05-33" src="https://github.com/user-attachments/assets/ad4f8720-ad06-4770-b6e6-84d366fa0fe7" />




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="514" height="62" alt="Screenshot from 2025-09-18 03-05-52" src="https://github.com/user-attachments/assets/7a55044c-ac84-4fd7-aaaf-91e268b1e22c" />


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

<img width="514" height="62" alt="Screenshot from 2025-09-18 03-10-23" src="https://github.com/user-attachments/assets/d16a99a2-1995-440e-a129-a02c87e6f7c5" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="514" height="62" alt="Screenshot from 2025-09-18 03-10-44" src="https://github.com/user-attachments/assets/208170a3-f509-4d7d-9dd7-7f476fa4d724" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="514" height="62" alt="Screenshot from 2025-09-18 03-11-09" src="https://github.com/user-attachments/assets/cf8ecb3d-8c7e-45ed-b04f-5628f24afe26" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="522" height="44" alt="Screenshot from 2025-09-18 03-11-33" src="https://github.com/user-attachments/assets/02d055a0-a0c3-463e-82dd-302f7aed4583" />


egrep '(world$)' newfile 
## OUTPUT
<img width="516" height="62" alt="Screenshot from 2025-09-18 03-12-02" src="https://github.com/user-attachments/assets/069eebaf-4757-4ce3-88a9-ae4d2f2ae5c4" />



egrep '(World$)' newfile 
## OUTPUT
<img width="515" height="40" alt="Screenshot from 2025-09-18 03-12-31" src="https://github.com/user-attachments/assets/465e04c3-3ce0-40c9-b8d7-ca49136ab4d7" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="516" height="79" alt="Screenshot from 2025-09-18 03-13-03" src="https://github.com/user-attachments/assets/e6b82701-53e3-4b56-885c-d7126e96e8e3" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="525" height="45" alt="Screenshot from 2025-09-18 03-13-34" src="https://github.com/user-attachments/assets/f8198199-3ef7-45bb-bb0b-9ceda063b103" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="525" height="45" alt="Screenshot from 2025-09-18 03-13-54" src="https://github.com/user-attachments/assets/8d6bbe75-309a-466b-b6ae-e8766ec924fd" />



egrep l{2} newfile
## OUTPUT

<img width="526" height="60" alt="Screenshot from 2025-09-18 03-15-50" src="https://github.com/user-attachments/assets/444627b2-35cd-4a9b-b73a-b43bbf00c122" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="523" height="79" alt="Screenshot from 2025-09-18 03-16-12" src="https://github.com/user-attachments/assets/e54a9ddd-de3e-4fbc-af2e-44935b906c5a" />


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
<img width="519" height="40" alt="Screenshot from 2025-09-18 03-20-09" src="https://github.com/user-attachments/assets/2b5c4a52-e35f-475f-a02b-30327864c6aa" />



sed -n -e '$p' file23
## OUTPUT
<img width="519" height="40" alt="Screenshot from 2025-09-18 03-20-34" src="https://github.com/user-attachments/assets/4076705e-5d09-4db8-bfd6-0671cd001a9b" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="519" height="187" alt="Screenshot from 2025-09-18 03-21-18" src="https://github.com/user-attachments/assets/3b46a11b-5aa2-4c65-9832-b44285dadcfc" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="519" height="187" alt="Screenshot from 2025-09-18 03-21-37" src="https://github.com/user-attachments/assets/f489b603-0600-4cfa-ac0c-52b67053fcd5" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="519" height="187" alt="Screenshot from 2025-09-18 03-21-58" src="https://github.com/user-attachments/assets/1fc3c282-2e3c-40a3-be47-b15ac5c66165" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="504" height="118" alt="Screenshot from 2025-09-18 03-22-21" src="https://github.com/user-attachments/assets/b37f7d86-db7e-45bc-b4e6-8ebddba75f37" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="500" height="80" alt="Screenshot from 2025-09-18 03-23-10" src="https://github.com/user-attachments/assets/ccfce1cb-0cf7-4093-8bea-68a7470e9cdf" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="503" height="65" alt="Screenshot from 2025-09-18 03-23-38" src="https://github.com/user-attachments/assets/3c08eebf-2680-4c43-8305-7167c3e8db11" />



seq 10 
## OUTPUT
<img width="485" height="206" alt="Screenshot from 2025-09-18 03-23-54" src="https://github.com/user-attachments/assets/6ab30581-ceb7-4d1a-9838-cce07775fa0e" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="485" height="80" alt="Screenshot from 2025-09-18 03-24-15" src="https://github.com/user-attachments/assets/193b29f1-99ce-476f-aa4e-655d1204a494" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="485" height="80" alt="Screenshot from 2025-09-18 03-24-36" src="https://github.com/user-attachments/assets/01fb9122-8e3e-452e-a1c9-fbcc3742a44f" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="484" height="105" alt="Screenshot from 2025-09-18 03-24-56" src="https://github.com/user-attachments/assets/745bdd77-3b69-4148-9927-8cc3254c9349" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="479" height="87" alt="Screenshot from 2025-09-18 03-25-23" src="https://github.com/user-attachments/assets/0cc1fc75-af50-46af-8314-147eb99e087c" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="479" height="87" alt="Screenshot from 2025-09-18 03-25-53" src="https://github.com/user-attachments/assets/8b55b58a-9e43-4f25-8d92-6ba74f8e59e7" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="477" height="78" alt="Screenshot from 2025-09-18 03-26-20" src="https://github.com/user-attachments/assets/68fa2c1e-1a58-4e46-936e-4af8c7a93200" />


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
<img width="475" height="116" alt="Screenshot from 2025-09-18 03-28-08" src="https://github.com/user-attachments/assets/fe5b40d9-b283-426d-90b5-4ab0b451fada" />


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
<img width="475" height="134" alt="Screenshot from 2025-09-18 03-29-47" src="https://github.com/user-attachments/assets/413bbdb0-e999-43eb-805e-cae455af1faf" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="547" height="188" alt="Screenshot from 2025-09-18 03-30-25" src="https://github.com/user-attachments/assets/25e44eb0-6e6a-49dc-b1d2-25d26f345472" />


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
<img width="523" height="80" alt="Screenshot from 2025-09-18 03-32-21" src="https://github.com/user-attachments/assets/94912836-7c28-4df3-9cdc-613c6e24bbc5" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="577" height="79" alt="Screenshot from 2025-09-18 03-33-28" src="https://github.com/user-attachments/assets/cf4f7dbb-f002-4118-8d0b-7652c56bc5d7" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="363" height="873" alt="Screenshot from 2025-09-16 01-10-52" src="https://github.com/user-attachments/assets/787df8f5-4e55-4ac0-8624-60d15da28a41" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -xvf backup.tar
## OUTPUT
<img width="307" height="174" alt="Screenshot from 2025-09-18 05-28-32" src="https://github.com/user-attachments/assets/996fdc7d-448a-4535-967c-6a68b595ae6b" />

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT
<img width="421" height="98" alt="Screenshot from 2025-09-18 05-28-55" src="https://github.com/user-attachments/assets/a545ad19-3e92-4006-b8cc-5330d13abab4" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World'; exit 0 >> my-script.sh
```
chmod 755 my-script.sh  ./my-script.sh

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="576" height="85" alt="Screenshot from 2025-09-18 03-41-24" src="https://github.com/user-attachments/assets/354dde61-5f87-49f9-b5fc-4d2ed20e6c64" />


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
<img width="529" height="257" alt="Screenshot from 2025-09-18 03-49-45" src="https://github.com/user-attachments/assets/be8685e4-b087-4c20-8e44-7f27e11ea503" />

 
ls file1
## OUTPUT
<img width="576" height="45" alt="Screenshot from 2025-09-18 03-46-42" src="https://github.com/user-attachments/assets/22bd25f2-7cb0-4951-bd48-cd12c8625c77" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="576" height="45" alt="Screenshot from 2025-09-18 03-46-50" src="https://github.com/user-attachments/assets/a4110b45-23a0-4d1d-9bc2-522603089d46" />

abcd
 
echo $?
 ## OUTPUT
<img width="506" height="42" alt="Screenshot from 2025-09-18 03-51-27" src="https://github.com/user-attachments/assets/3a879bb5-49e6-4233-ae7e-90818094a391" />


 
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

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="573" height="58" alt="Screenshot from 2025-09-18 03-55-08" src="https://github.com/user-attachments/assets/952dac5d-b408-4ce8-ba2f-90e65e57411b" />


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
<img width="593" height="66" alt="Screenshot from 2025-09-18 03-56-46" src="https://github.com/user-attachments/assets/3def3a31-9e5c-48b9-8253-6b81d8195e87" />

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

<img width="589" height="117" alt="Screenshot from 2025-09-18 03-58-29" src="https://github.com/user-attachments/assets/6720aba4-e5fd-451b-ae53-8f064ae8ee16" />


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

## OUTPUT
<img width="606" height="80" alt="Screenshot from 2025-09-18 03-59-39" src="https://github.com/user-attachments/assets/c4a62d6c-2a30-4956-8ddf-331efdbb4313" />

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
## OUTPUT
<img width="613" height="117" alt="Screenshot from 2025-09-18 04-00-39" src="https://github.com/user-attachments/assets/a58af1e3-4693-4c32-aea1-0c944bf783d4" />

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
<img width="617" height="65" alt="Screenshot from 2025-09-18 04-01-38" src="https://github.com/user-attachments/assets/31648498-fec5-467d-af5c-98c9c2f5946d" />


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
<img width="617" height="65" alt="Screenshot from 2025-09-18 04-02-35" src="https://github.com/user-attachments/assets/e4c824bc-99a1-4527-b2d6-c89d00b7145d" />

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
## OUTPUT
<img width="617" height="65" alt="Screenshot from 2025-09-18 04-04-29" src="https://github.com/user-attachments/assets/b71f3f37-fc4f-4c06-9bc2-eeb26aee0923" />

 
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
 ## OUTPUT
 <img width="592" height="207" alt="Screenshot from 2025-09-18 04-06-06" src="https://github.com/user-attachments/assets/c8bdfe53-7221-42d7-b597-b25d2761d977" />

 
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
$ ./untiltest.sh
## OUTPUT
 <img width="590" height="118" alt="Screenshot from 2025-09-18 04-07-57" src="https://github.com/user-attachments/assets/02fc7256-0bed-475f-ad0b-5e4a7c1c1c54" />

 
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
$ ./forin1.sh
## OUTPUT
<img width="590" height="167" alt="Screenshot from 2025-09-18 04-09-42" src="https://github.com/user-attachments/assets/46203a4d-5157-443f-bf13-f871c136103c" />

 
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
## OUTPUT
<img width="590" height="120" alt="Screenshot from 2025-09-18 04-10-52" src="https://github.com/user-attachments/assets/c2dcd738-8c4a-4a06-b640-c76ea892915e" />


 
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
 ## OUTPUT
<img width="603" height="169" alt="Screenshot from 2025-09-18 04-12-03" src="https://github.com/user-attachments/assets/d5393e17-3c43-48cd-a17e-463b5e59c9e8" />

 
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
<img width="609" height="154" alt="Screenshot from 2025-09-18 04-18-29" src="https://github.com/user-attachments/assets/559677ff-9323-48f3-86dd-e832bd26fcdb" />


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
<img width="611" height="116" alt="Screenshot from 2025-09-18 04-19-29" src="https://github.com/user-attachments/assets/50032e69-1958-49c7-a4df-758a7e0a459b" />

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
<img width="611" height="116" alt="Screenshot from 2025-09-18 04-23-01" src="https://github.com/user-attachments/assets/8cad211c-18fb-4573-a40c-4f92b3901c0c" />

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
<img width="600" height="241" alt="Screenshot from 2025-09-18 04-23-56" src="https://github.com/user-attachments/assets/f0e3f53c-e450-4c2b-b225-ab34883a0c62" />

 
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
## OUTPUT
<img width="597" height="77" alt="Screenshot from 2025-09-18 04-25-01" src="https://github.com/user-attachments/assets/7fc7479c-9e48-4ebf-81c7-3c80791937a4" />

cat forcontinue.sh
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
$ chmod 755 forcontinue.sh
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 <img width="596" height="116" alt="Screenshot from 2025-09-18 04-29-32" src="https://github.com/user-attachments/assets/107c593e-d419-4086-9177-4118e70e43e3" />

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
<img width="593" height="60" alt="Screenshot from 2025-09-18 04-30-36" src="https://github.com/user-attachments/assets/d5a69374-2223-4ee5-bed3-e8bbc01a3164" />



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
<img width="600" height="80" alt="Screenshot from 2025-09-18 04-32-53" src="https://github.com/user-attachments/assets/69285a27-6d1f-46e9-94fc-84bbf3cf0cc4" />




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
 ./funcex.sh 
 ## OUTPUT
<img width="600" height="45" alt="Screenshot from 2025-09-18 04-33-43" src="https://github.com/user-attachments/assets/67822c89-8456-4cb5-a719-ecd4dbcc774b" />

 
 ./funcex.sh 1 2
 ## OUTPUT
 <img width="600" height="45" alt="Screenshot from 2025-09-18 04-34-31" src="https://github.com/user-attachments/assets/2b981bbf-9a24-44db-8e1a-c080405c5f11" />


 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
 ## OUTPUT
<img width="595" height="79" alt="Screenshot from 2025-09-18 04-35-41" src="https://github.com/user-attachments/assets/87e445ff-4f84-4900-8138-c993ef61f486" />

 
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
$ chmod 777 argshift1.sh
$ ./argshift1.sh 1 2 3
## OUTPUT
<img width="595" height="79" alt="Screenshot from 2025-09-18 04-36-37" src="https://github.com/user-attachments/assets/0156c589-0f41-4146-a240-0731c609782b" />

 
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
 ./argshift.sh 1 2 3
 ## OUTPUT
 <img width="597" height="277" alt="Screenshot from 2025-09-18 04-37-59" src="https://github.com/user-attachments/assets/a54b2dd8-89ee-48dc-b023-4b1dec20952d" />

 
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
 <img width="597" height="262" alt="Screenshot from 2025-09-18 04-39-58" src="https://github.com/user-attachments/assets/1bcba14f-0e4d-4645-a184-f8e7e532c9f8" />

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
<img width="588" height="80" alt="Screenshot from 2025-09-18 04-41-59" src="https://github.com/user-attachments/assets/80e15e41-920e-4c0f-8094-4d566a801e63" />


# RESULT:
The Commands are executed successfully.
