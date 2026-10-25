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

<img width="664" height="134" alt="Screenshot from 2026-10-23 10-54-37" src="https://github.com/user-attachments/assets/0a34773f-1200-4125-bbc1-66e94d3c8b34" />


cat < file2
## OUTPUT
<img width="666" height="139" alt="Screenshot from 2026-10-23 10-54-51" src="https://github.com/user-attachments/assets/0d1e8c87-8853-4149-ae9e-98c8ca08ed2f" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="666" height="139" alt="Screenshot from 2026-10-23 10-59-37" src="https://github.com/user-attachments/assets/00ff2677-cd50-4f02-becf-466936ed572b" />

comm file1 file2
 ## OUTPUT
<img width="660" height="206" alt="Screenshot from 2026-10-23 11-00-18" src="https://github.com/user-attachments/assets/d4285b15-e1de-4f73-a400-70727fe79157" />

 

diff file1 file2
## OUTPUT
<img width="658" height="252" alt="Screenshot from 2026-10-23 11-00-55" src="https://github.com/user-attachments/assets/cf42ae39-f79a-49dd-b320-bb4053a5bf28" />


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

<img width="658" height="252" alt="Screenshot from 2026-10-23 11-03-58" src="https://github.com/user-attachments/assets/5c29cbfe-05e2-449a-a325-3d66a9c92142" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="660" height="125" alt="Screenshot from 2026-10-23 11-04-40" src="https://github.com/user-attachments/assets/0d3abebb-83a3-4d45-b17b-64497104500f" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="660" height="125" alt="Screenshot from 2026-10-23 11-04-56" src="https://github.com/user-attachments/assets/fb2d5843-e8c1-481c-88e0-0e930a5216c1" />


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
<img width="660" height="125" alt="Screenshot from 2026-10-23 11-07-21" src="https://github.com/user-attachments/assets/4c82a935-96ba-4563-966f-ab7e6d65ac78" />



grep hello newfile 
## OUTPUT

<img width="660" height="125" alt="Screenshot from 2026-10-23 11-07-21" src="https://github.com/user-attachments/assets/3482cf7b-c96c-4a88-8cf8-b225cacbbaef" />



grep -v hello newfile 
## OUTPUT

<img width="660" height="81" alt="Screenshot from 2026-10-23 11-08-17" src="https://github.com/user-attachments/assets/96d00f6b-babc-4324-acee-e765903d59f1" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="660" height="81" alt="Screenshot from 2026-10-23 11-09-09" src="https://github.com/user-attachments/assets/9ee2d168-6604-4ca5-b36c-148e555d3539" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="660" height="81" alt="Screenshot from 2026-10-23 11-09-29" src="https://github.com/user-attachments/assets/5d93e202-0c8e-45c4-b8e4-2cafbb328a00" />


grep -R ubuntu /etc
## OUTPUT

<img width="825" height="612" alt="image" src="https://github.com/user-attachments/assets/8c0df4f5-5bbd-42d0-8466-d0a49dc77b2a" />


grep -w -n world newfile   
## OUTPUT
<img width="825" height="146" alt="image" src="https://github.com/user-attachments/assets/61782192-992d-4e8b-8d74-94ec10a55a4a" />


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

<img width="817" height="104" alt="image" src="https://github.com/user-attachments/assets/f0bfbd12-6cdb-47e2-8f2c-302319756cf7" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="817" height="104" alt="image" src="https://github.com/user-attachments/assets/5bdc6083-1b8f-4b8b-89ce-baf2393151a9" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="817" height="104" alt="image" src="https://github.com/user-attachments/assets/5c31bba6-2979-419c-86bb-1371d0045c3c" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="817" height="104" alt="image" src="https://github.com/user-attachments/assets/8951929e-8f23-4f33-bd35-de946b13f759" />


egrep '(world$)' newfile 
## OUTPUT

<img width="817" height="104" alt="image" src="https://github.com/user-attachments/assets/fe5d10b5-7b8b-4830-a092-c9b60b5fb17e" />


egrep '(World$)' newfile 
## OUTPUT

<img width="818" height="76" alt="image" src="https://github.com/user-attachments/assets/c2d6e25d-ea61-4a8e-bf52-613b502a5c72" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="818" height="79" alt="image" src="https://github.com/user-attachments/assets/8c4ae52c-dd34-4e3f-8921-ebdff3ae1491" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="818" height="79" alt="image" src="https://github.com/user-attachments/assets/36d0dba9-1949-418b-a815-081291c72d49" />


egrep 'Linux.*world' newfile 
## OUTPUT


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="818" height="79" alt="image" src="https://github.com/user-attachments/assets/1ecf942c-db47-44ae-99f0-7f6f04b5df9e" />


egrep l{2} newfile
## OUTPUT

<img width="817" height="89" alt="image" src="https://github.com/user-attachments/assets/0adfb507-64c0-4efe-99a7-93d685bd2acb" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="824" height="118" alt="image" src="https://github.com/user-attachments/assets/730e8643-1eed-4c4e-a636-bfef80f7175a" />


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
<img width="824" height="118" alt="image" src="https://github.com/user-attachments/assets/77b175cc-1e19-4874-b53e-63dc5abf60e0" />



sed -n -e '$p' file23
## OUTPUT
<img width="824" height="68" alt="image" src="https://github.com/user-attachments/assets/8f98a581-d5b3-462f-9252-32c031343756" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="825" height="225" alt="image" src="https://github.com/user-attachments/assets/86bade83-1037-4ae8-926b-e7534207ba08" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="825" height="225" alt="image" src="https://github.com/user-attachments/assets/caca7cae-40a9-4da5-bdcd-8b3fd083660a" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="825" height="225" alt="image" src="https://github.com/user-attachments/assets/03f06626-38a8-4ba2-9317-956cb171820e" />

sed -n -e '1,5p' file23
## OUTPUT

<img width="822" height="158" alt="image" src="https://github.com/user-attachments/assets/620101ba-326f-4455-824b-d406476fb9b2" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="822" height="158" alt="image" src="https://github.com/user-attachments/assets/85b83765-bf87-4ecd-8b5c-b422a1b89e56" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="822" height="158" alt="image" src="https://github.com/user-attachments/assets/4e85b165-f7a0-499c-916f-cf8dc6709bc3" />


seq 10 
## OUTPUT
<img width="836" height="270" alt="image" src="https://github.com/user-attachments/assets/3e542308-be77-40e2-bcb6-9f68697c6ca9" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="534" height="128" alt="image" src="https://github.com/user-attachments/assets/c9d728f6-8b6f-4490-a45d-37ab7774bd52" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="533" height="144" alt="image" src="https://github.com/user-attachments/assets/7ebd80e1-b59e-47c9-9486-8c3f0d310762" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="533" height="144" alt="image" src="https://github.com/user-attachments/assets/0e644ebe-3b9b-4e93-b1d4-ac43e8835fc0" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="533" height="144" alt="image" src="https://github.com/user-attachments/assets/b2da0254-eaaf-4d57-9f4e-def516969276" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="533" height="144" alt="image" src="https://github.com/user-attachments/assets/ef636131-7366-4c49-aae8-78e4379fae9f" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="531" height="163" alt="image" src="https://github.com/user-attachments/assets/a275dc88-f9ac-4d62-b8c9-34cfdb11731b" />


sed -n '2,4{s/$/*/;p}' file23
## output
<img width="531" height="163" alt="image" src="https://github.com/user-attachments/assets/37229a33-e357-43eb-900c-de05186d3b44" />


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
<img width="617" height="256" alt="image" src="https://github.com/user-attachments/assets/0e6b576c-9ca7-41a0-88e5-9a5f8043fca7" />


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

<img width="616" height="125" alt="image" src="https://github.com/user-attachments/assets/7a21372b-5400-4cc0-9f9e-449f88595bef" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="742" height="125" alt="image" src="https://github.com/user-attachments/assets/3258d493-3254-4099-a22f-5aec9b6f8b51" />

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

<img width="752" height="231" alt="image" src="https://github.com/user-attachments/assets/7527644f-ae3b-4fea-891b-748f898e0ed6" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="752" height="231" alt="image" src="https://github.com/user-attachments/assets/d435be33-d51d-4729-9645-bc9d756944a0" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="752" height="231" alt="image" src="https://github.com/user-attachments/assets/cea08316-637d-49d1-aaf8-b007d575116d" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="832" height="255" alt="image" src="https://github.com/user-attachments/assets/2322867b-2e81-4486-958a-49d657b681d9" />


tar -xvf backup.tar
## OUTPUT
<img width="832" height="255" alt="image" src="https://github.com/user-attachments/assets/ef1da4a6-72c8-4bed-8492-a7ba2dfc1973" />

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 <img width="832" height="255" alt="image" src="https://github.com/user-attachments/assets/d0dd7a75-9759-4ddb-abb8-8403d3d112f0" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="818" height="580" alt="image" src="https://github.com/user-attachments/assets/d526c95f-72aa-4406-b7f0-54cc736fe5af" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="818" height="580" alt="image" src="https://github.com/user-attachments/assets/5711621c-95c0-475f-9184-e6b13df6859e" />


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
<img width="818" height="580" alt="image" src="https://github.com/user-attachments/assets/8623244c-9d88-467c-9156-c47a93904f4b" />

 
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

<img width="830" height="867" alt="image" src="https://github.com/user-attachments/assets/f8d26471-a46d-4b24-a812-bd9413cc905c" />

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
<img width="830" height="867" alt="image" src="https://github.com/user-attachments/assets/60a292d9-5d50-4615-8ddf-fef4a4b09ae2" />

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
<img width="830" height="867" alt="image" src="https://github.com/user-attachments/assets/2225c1a8-e5dd-427c-9696-4d97f9da280a" />

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
<img width="819" height="667" alt="image" src="https://github.com/user-attachments/assets/c84b2eef-0066-4f71-ad5e-335ee53e4d1b" />

 
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
![Uploading image.png…]()

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
 <img width="819" height="562" alt="image" src="https://github.com/user-attachments/assets/bf6b2298-9e44-49df-85c7-88695c2e2f33" />

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
<img width="832" height="277" alt="image" src="https://github.com/user-attachments/assets/73c609f8-a7ee-411d-9627-284961f69f60" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="832" height="277" alt="image" src="https://github.com/user-attachments/assets/9e094817-b55f-4647-915d-52731334fc6a" />


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
<img width="819" height="562" alt="image" src="https://github.com/user-attachments/assets/80db906c-15d2-4433-b71f-d35b138498ab" />

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
 <img width="819" height="562" alt="image" src="https://github.com/user-attachments/assets/8af42131-e0eb-408c-a8f6-a72a0ff20457" />

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
 
 ![Uploading image.png…]()

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
 ![Uploading image.png…]()

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

![Uploading image.png…]()

# RESULT:
The Commands are executed successfully.
