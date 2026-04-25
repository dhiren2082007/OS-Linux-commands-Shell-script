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
<img width="382" height="125" alt="Screenshot 2026-04-25 114947" src="https://github.com/user-attachments/assets/c45077da-3f9d-4947-a491-fc86d1a76d9b" />


cat < file2
## OUTPUT
<img width="317" height="144" alt="Screenshot 2026-04-25 115120" src="https://github.com/user-attachments/assets/ae2a5834-eb0b-4d5e-a802-a1cd1d6e0735" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="597" height="305" alt="Screenshot 2026-04-25 115256" src="https://github.com/user-attachments/assets/d673f6ac-8b7d-4c40-bbce-d3d961d152d9" />

comm file1 file2
 ## OUTPUT
<img width="602" height="282" alt="Screenshot 2026-04-25 115341" src="https://github.com/user-attachments/assets/7f4b3937-d171-46a7-9391-88489a2627c3" />

 
diff file1 file2
## OUTPUT
<img width="1280" height="578" alt="WhatsApp Image 2026-02-22 at 11 03 58 PM" src="https://github.com/user-attachments/assets/b30fc42e-49aa-4c68-a7a9-ed2b63265064" />


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
<img width="459" height="94" alt="image" src="https://github.com/user-attachments/assets/fa26cab9-f51c-44ed-9a90-8ea0f0ae4be0" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="395" height="125" alt="image" src="https://github.com/user-attachments/assets/b0f42ab5-e949-453c-8d24-481be25d70b2" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="426" height="138" alt="image" src="https://github.com/user-attachments/assets/a6d5ff9e-b5f9-44fd-984d-6a4838d65d8b" />

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
<img width="301" height="76" alt="image" src="https://github.com/user-attachments/assets/f0b58fa8-c734-42cf-9144-684171354923" />



grep hello newfile 
## OUTPUT

<img width="393" height="83" alt="image" src="https://github.com/user-attachments/assets/b6a7e359-5d50-48e3-86f4-0781ec51c22e" />



grep -v hello newfile 
## OUTPUT
<img width="440" height="77" alt="image" src="https://github.com/user-attachments/assets/d2da09e4-5dda-42c4-b880-6207052deb17" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="488" height="104" alt="image" src="https://github.com/user-attachments/assets/ebfc59e2-e87c-4b19-bedb-0987b41771fd" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="408" height="75" alt="image" src="https://github.com/user-attachments/assets/210973a4-f398-4869-b9fe-4ce908fe6f9a" />



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="437" height="98" alt="image" src="https://github.com/user-attachments/assets/5f6199b1-8002-4342-92b9-3f6efcd0d8a2" />



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
<img width="657" height="101" alt="image" src="https://github.com/user-attachments/assets/fa3705e9-1055-4d67-a09f-e8de4f47398a" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="480" height="100" alt="image" src="https://github.com/user-attachments/assets/ce1a3d04-de81-4db4-ab02-61f52ec83197" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="478" height="114" alt="image" src="https://github.com/user-attachments/assets/9c57950e-6327-41e9-a3a7-6f302c6d0ea1" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="501" height="87" alt="image" src="https://github.com/user-attachments/assets/7d7b408f-50fa-4628-94f4-d30fee00cac4" />



egrep '(world$)' newfile 
## OUTPUT

<img width="489" height="110" alt="image" src="https://github.com/user-attachments/assets/db9a6c35-7e7b-437d-bfcd-498222e6e88f" />


egrep '(World$)' newfile 
## OUTPUT
<img width="524" height="71" alt="image" src="https://github.com/user-attachments/assets/b796462c-f3b0-4c68-8a53-460a8ec61dfa" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="480" height="135" alt="image" src="https://github.com/user-attachments/assets/79fd59bc-0c2a-408d-9f44-0a80bbcbd7b6" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="408" height="78" alt="image" src="https://github.com/user-attachments/assets/212381c8-e418-48be-8ffc-376202318f10" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="447" height="89" alt="image" src="https://github.com/user-attachments/assets/217ef849-b34f-49be-88ec-ab19bbf67d2f" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="386" height="73" alt="image" src="https://github.com/user-attachments/assets/17a96bdd-6ed2-4018-be9d-c1ef63cfbae4" />


egrep l{2} newfile
## OUTPUT
<img width="300" height="102" alt="image" src="https://github.com/user-attachments/assets/c349b453-534b-426a-bf89-1f93179f0850" />




egrep 's{1,2}' newfile
## OUTPUT 
<img width="477" height="129" alt="image" src="https://github.com/user-attachments/assets/060b00bb-cb74-480c-8127-acf0d6b57ba4" />


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
<img width="515" height="94" alt="image" src="https://github.com/user-attachments/assets/19868660-8d3a-40f5-b239-f5bdf29201a2" />



sed -n -e '$p' file23
## OUTPUT
<img width="527" height="78" alt="image" src="https://github.com/user-attachments/assets/012c2a7d-1681-4c4e-a78d-2745aa5d4db3" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="527" height="247" alt="image" src="https://github.com/user-attachments/assets/9f140ae2-07c6-4f0d-8c9f-a3fad3475910" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="511" height="261" alt="image" src="https://github.com/user-attachments/assets/569f69f4-1fdb-4a54-836c-2900dea0a25f" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="470" height="242" alt="image" src="https://github.com/user-attachments/assets/b56ff989-62fd-48e7-a741-41ca239c7fba" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="534" height="184" alt="image" src="https://github.com/user-attachments/assets/609c90cf-ef00-4564-a761-a9ff035080fc" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="443" height="143" alt="image" src="https://github.com/user-attachments/assets/9039ed25-d3e0-414e-b506-ac9086147493" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="607" height="113" alt="image" src="https://github.com/user-attachments/assets/df5d9c33-2bdf-4915-a599-c69c81d08e26" />


seq 10 
## OUTPUT
<img width="460" height="294" alt="image" src="https://github.com/user-attachments/assets/f3b8f096-a2bb-48cb-8ecb-965243049df3" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="440" height="128" alt="image" src="https://github.com/user-attachments/assets/8bfd6dcc-ae78-449c-acf5-f2aeebec988e" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="361" height="119" alt="image" src="https://github.com/user-attachments/assets/77daeb09-7c75-4b3c-adb7-d8885c693a39" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="400" height="162" alt="image" src="https://github.com/user-attachments/assets/9da4a2e2-ad84-4b39-baf3-0cc25b6d7fa3" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="538" height="127" alt="image" src="https://github.com/user-attachments/assets/d87d690c-ea43-47fb-afe6-eefd64a0255e" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="582" height="129" alt="image" src="https://github.com/user-attachments/assets/1a7fc848-a148-4a71-9fdc-cf38bd1471ed" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="603" height="126" alt="image" src="https://github.com/user-attachments/assets/305c46b9-3bb9-4473-b97b-4e40137705c4" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="598" height="144" alt="image" src="https://github.com/user-attachments/assets/28e0e334-ab01-4bdc-8fc7-d160617a393c" />



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
<img width="455" height="177" alt="image" src="https://github.com/user-attachments/assets/96ad6a18-5d52-40ec-9d6c-573394596af2" />


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
<img width="437" height="187" alt="image" src="https://github.com/user-attachments/assets/a2975632-68be-458a-b174-4858993f2d80" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="516" height="241" alt="image" src="https://github.com/user-attachments/assets/9b00e10b-ca46-4315-8d05-50e71f87ba60" />


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
<img width="509" height="129" alt="image" src="https://github.com/user-attachments/assets/89badac0-345b-45b8-be61-6c354ce367ce" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="640" height="123" alt="image" src="https://github.com/user-attachments/assets/47bbe2e8-a266-4bac-b024-42995bacae25" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="736" height="355" alt="image" src="https://github.com/user-attachments/assets/3472e77c-e08f-4063-959f-3fc1c67a4541" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="797" height="265" alt="image" src="https://github.com/user-attachments/assets/5c04f5b2-9fd3-4d0e-8f24-28815dc3be3b" />



tar -xvf backup.tar
## OUTPUT
<img width="778" height="283" alt="image" src="https://github.com/user-attachments/assets/6c0433ab-20d4-4a43-b7cc-52aa0f123250" />

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
<img width="498" height="112" alt="image" src="https://github.com/user-attachments/assets/d5fd9e6a-0169-492a-a2b4-a4dd06237e3b" />


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
<img width="800" height="409" alt="image" src="https://github.com/user-attachments/assets/91c61118-ace7-467b-ab24-43da213a85c7" />

 
ls file1
## OUTPUT
<img width="400" height="69" alt="image" src="https://github.com/user-attachments/assets/3b8b858d-9bb8-48d8-bcaa-ed654d162aa2" />

echo $?
## OUTPUT
<img width="351" height="84" alt="image" src="https://github.com/user-attachments/assets/f8ac8de4-7a00-4009-b63d-4ce9eb26321d" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="461" height="89" alt="image" src="https://github.com/user-attachments/assets/b2e30576-bf4c-400c-a0ea-1e656b08eae8" />

abcd
 
echo $?
 ## OUTPUT
<img width="432" height="68" alt="image" src="https://github.com/user-attachments/assets/367b9f20-4f89-4496-913a-555f270e282f" />


 
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
<img width="775" height="105" alt="image" src="https://github.com/user-attachments/assets/0a8be191-26fa-477c-a173-35b3c9201b81" />


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
<img width="790" height="242" alt="image" src="https://github.com/user-attachments/assets/e3feccf3-fe86-4f9e-bdf0-d49e2e8bc3be" />

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

<img width="597" height="74" alt="image" src="https://github.com/user-attachments/assets/dd6fe032-a7b7-4ca5-9fb2-45b60b4e9a9d" />


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
