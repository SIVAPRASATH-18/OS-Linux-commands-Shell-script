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
<img width="548" height="120" alt="Screenshot 2026-04-25 135523" src="https://github.com/user-attachments/assets/bfe14f9b-1150-45e3-acd1-259b4a665d80" />

cat < file2
## OUTPUT
<img width="558" height="150" alt="Screenshot 2026-04-25 135611" src="https://github.com/user-attachments/assets/f274d255-d99f-4232-8b5d-e4690352f1a4" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="577" height="71" alt="Screenshot 2026-04-25 135707" src="https://github.com/user-attachments/assets/aa38cb8d-f5c4-4077-bb63-c572bd124e99" />


comm file1 file2
 ## OUTPUT
<img width="649" height="225" alt="Screenshot 2026-04-25 140058" src="https://github.com/user-attachments/assets/eb7ee134-3100-4136-84a6-4cabdb45c387" />

 
diff file1 file2
## OUTPUT
<img width="579" height="232" alt="Screenshot 2026-04-25 135825" src="https://github.com/user-attachments/assets/1b100db0-fa91-4782-b3f8-0988226b51f3" />


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
<img width="597" height="87" alt="Screenshot 2026-04-25 140239" src="https://github.com/user-attachments/assets/d6e95f4b-ef00-4f80-a1d0-7686c8409b42" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="617" height="116" alt="Screenshot 2026-04-25 140336" src="https://github.com/user-attachments/assets/13bebd6a-22e5-4a72-8bea-4238ed2bd795" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="662" height="112" alt="Screenshot 2026-04-25 140344" src="https://github.com/user-attachments/assets/e756f491-be72-4909-b1f2-0e5897f21b42" />


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
<img width="611" height="63" alt="Screenshot 2026-04-25 140445" src="https://github.com/user-attachments/assets/1af9d277-63a5-446a-b412-af739bf4ae38" />

grep hello newfile 
## OUTPUT
<img width="597" height="68" alt="Screenshot 2026-04-25 140436" src="https://github.com/user-attachments/assets/ba22eca3-a168-4c30-8c72-df1f563dcd9f" />


grep -v hello newfile 
## OUTPUT

<img width="606" height="60" alt="Screenshot 2026-04-25 140535" src="https://github.com/user-attachments/assets/ea4861af-a684-4035-b072-a4437aea8214" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="715" height="107" alt="Screenshot 2026-04-25 140619" src="https://github.com/user-attachments/assets/78a41055-158b-4268-a87b-fb50847b0a0c" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="692" height="77" alt="Screenshot 2026-04-25 140627" src="https://github.com/user-attachments/assets/7dac1660-4bf6-44b3-9119-209cf2fa6228" />


grep -R ubuntu /etc
## OUTPUT

<img width="937" height="169" alt="Screenshot 2026-04-25 140852" src="https://github.com/user-attachments/assets/4aec92d5-707d-4a06-84cc-0e95281f0920" />
<img width="699" height="117" alt="Screenshot 2026-04-25 140915" src="https://github.com/user-attachments/assets/d0f91eea-c0c4-4c47-be03-ffbbf5514dca" />


grep -w -n world newfile   
## OUTPUT

<img width="660" height="101" alt="Screenshot 2026-04-25 140638" src="https://github.com/user-attachments/assets/408c339f-782f-4d57-a876-496c792c4be0" />

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
<img width="633" height="93" alt="Screenshot 2026-04-25 141020" src="https://github.com/user-attachments/assets/3c5c33db-614b-4cac-a306-ef95b1533864" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="623" height="87" alt="Screenshot 2026-04-25 141027" src="https://github.com/user-attachments/assets/94b025be-973b-4c0d-b034-19d8ecb54651" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="656" height="94" alt="Screenshot 2026-04-25 141033" src="https://github.com/user-attachments/assets/0a834b97-edb7-4292-8fbe-89b5f53e1dd6" />



egrep '(^hello)' newfile 
## OUTPUT


<img width="697" height="72" alt="Screenshot 2026-04-25 141038" src="https://github.com/user-attachments/assets/1a961c25-ad5a-4039-8242-8270c7681779" />

egrep '(world$)' newfile 
## OUTPUT
<img width="599" height="88" alt="Screenshot 2026-04-25 141157" src="https://github.com/user-attachments/assets/ec0791b6-95ea-4469-a220-8a083b394316" />



egrep '(World$)' newfile 
## OUTPUT
<img width="606" height="74" alt="Screenshot 2026-04-25 141213" src="https://github.com/user-attachments/assets/408e293c-a780-41c5-b0af-937ca38ff87a" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="609" height="123" alt="Screenshot 2026-04-25 141231" src="https://github.com/user-attachments/assets/065fe76c-18f0-4de6-a3a3-1b160bead949" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="614" height="77" alt="Screenshot 2026-04-25 141357" src="https://github.com/user-attachments/assets/ec03fd63-b9f1-422e-ab5f-450c71ed71d2" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="609" height="81" alt="Screenshot 2026-04-25 141429" src="https://github.com/user-attachments/assets/c7de2674-15b1-40f8-a32c-201f14f78d93" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="612" height="61" alt="Screenshot 2026-04-25 141437" src="https://github.com/user-attachments/assets/8a8f9b72-4d6d-45c4-85ce-1276816e00e2" />


egrep l{2} newfile
## OUTPUT
<img width="634" height="83" alt="Screenshot 2026-04-25 141446" src="https://github.com/user-attachments/assets/c61e2247-5c8b-4abc-af3a-6e5d5645f167" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="745" height="131" alt="Screenshot 2026-04-25 141607" src="https://github.com/user-attachments/assets/ba339226-4669-44f5-88ff-fbeacb043403" />


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
<img width="743" height="76" alt="Screenshot 2026-04-25 141626" src="https://github.com/user-attachments/assets/50f79a73-1956-4565-9485-55f1d60eba89" />


sed -n -e '$p' file23
## OUTPUT
<img width="686" height="80" alt="Screenshot 2026-04-25 141632" src="https://github.com/user-attachments/assets/cf81132a-658b-4794-a9c3-ff764234e79e" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="575" height="200" alt="Screenshot 2026-04-25 141802" src="https://github.com/user-attachments/assets/51f0b075-da7a-4235-9e57-cd9bc5184bf4" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="580" height="208" alt="Screenshot 2026-04-25 141807" src="https://github.com/user-attachments/assets/53a4b3d5-2641-4743-a30e-885fb7436e0e" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="646" height="196" alt="Screenshot 2026-04-25 141813" src="https://github.com/user-attachments/assets/3be370b8-edb7-4e2f-8822-48816f9b0867" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="628" height="167" alt="Screenshot 2026-04-25 141915" src="https://github.com/user-attachments/assets/6e832ad3-581f-439b-a71f-14a7c29c2102" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="654" height="135" alt="Screenshot 2026-04-25 141922" src="https://github.com/user-attachments/assets/31dbad12-6edb-4689-aa65-deb3b133e3e6" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="675" height="90" alt="Screenshot 2026-04-25 141928" src="https://github.com/user-attachments/assets/b9e5f00a-a535-40d3-9ca1-dacb374b0ad5" />



seq 10 
## OUTPUT
<img width="669" height="329" alt="Screenshot 2026-04-25 142243" src="https://github.com/user-attachments/assets/6e8b33e8-5e20-4e54-b124-e354581bf4cd" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="672" height="158" alt="Screenshot 2026-04-25 142252" src="https://github.com/user-attachments/assets/0cad94c8-5bef-4431-a4b9-ff5a93884718" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="739" height="122" alt="Screenshot 2026-04-25 142258" src="https://github.com/user-attachments/assets/650da5a9-01ce-4924-80b5-c6d1b1353c66" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="668" height="139" alt="Screenshot 2026-04-25 142724" src="https://github.com/user-attachments/assets/556a0469-d244-4816-aded-320bdb025f27" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="704" height="138" alt="Screenshot 2026-04-25 142444" src="https://github.com/user-attachments/assets/341ca365-b8de-4ece-a2c0-f91f976c718a" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="659" height="129" alt="Screenshot 2026-04-25 142802" src="https://github.com/user-attachments/assets/181ee23e-cd3b-4fda-903e-b5c12924c2ea" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="702" height="139" alt="Screenshot 2026-04-25 142926" src="https://github.com/user-attachments/assets/1491d83a-2e99-443f-bed9-03e1f8654ac2" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="672" height="149" alt="Screenshot 2026-04-25 142933" src="https://github.com/user-attachments/assets/9d8ba72b-1a5e-4404-814c-0d347d2d4444" />


## Sorting File content
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
<img width="729" height="164" alt="Screenshot 2026-04-25 143133" src="https://github.com/user-attachments/assets/01c29d82-0ab9-416f-a2ee-56055b2ad9ed" />


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
<img width="681" height="173" alt="Screenshot 2026-04-25 143202" src="https://github.com/user-attachments/assets/8fbb6951-4f4d-48ea-916b-718e5ef25af2" />



## Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="777" height="267" alt="Screenshot 2026-04-25 143207" src="https://github.com/user-attachments/assets/4e4e2acf-027f-4762-98da-f107a9e7ed98" />


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
<img width="728" height="123" alt="Screenshot 2026-04-25 143344" src="https://github.com/user-attachments/assets/a754148a-7fb5-409f-b696-5a1d0857068f" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="668" height="132" alt="Screenshot 2026-04-25 143351" src="https://github.com/user-attachments/assets/d423187b-3ded-45cf-9870-cb2d4f79539d" />



## Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="576" height="239" alt="Screenshot 2026-04-25 143446" src="https://github.com/user-attachments/assets/78e79169-898e-4960-891f-83644351ce23" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="686" height="252" alt="Screenshot 2026-04-25 143518" src="https://github.com/user-attachments/assets/49a490d5-bd44-40ce-b6d3-b8309a152668" />


tar -xvf backup.tar
## OUTPUT
<img width="780" height="303" alt="Screenshot 2026-04-25 143601" src="https://github.com/user-attachments/assets/90421272-7987-407a-81de-f8f196695f73" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="827" height="130" alt="Screenshot 2026-04-25 144800" src="https://github.com/user-attachments/assets/369a005b-ca28-4f70-aa02-c7cc795914a9" />

 
gunzip backup.tar.gz
## OUTPUT
<img width="711" height="81" alt="Screenshot 2026-04-25 145229" src="https://github.com/user-attachments/assets/03e218e7-cde4-4b41-b1fd-61a380253147" />
 
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
