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

<img width="321" height="125" alt="Screenshot 2026-07-24 214207" src="https://github.com/user-attachments/assets/0a8007c8-66f3-4875-b9e1-35b5ba1ff4fc" />


cat < file2
## OUTPUT
<img width="332" height="142" alt="Screenshot 2026-07-24 214229" src="https://github.com/user-attachments/assets/82c5d3bc-4bf0-4f5f-a39a-b987f107ee9f" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="377" height="63" alt="Screenshot 2026-07-24 214250" src="https://github.com/user-attachments/assets/0aaa6690-6d50-4f38-ae38-0a33c7695cd7" />

comm file1 file2
 ## OUTPUT
<img width="415" height="188" alt="Screenshot 2026-07-24 214314" src="https://github.com/user-attachments/assets/03836a69-1809-4e20-adf4-e5c278eea354" />

 
diff file1 file2
## OUTPUT
<img width="408" height="223" alt="Screenshot 2026-07-24 214339" src="https://github.com/user-attachments/assets/4391bfa8-1882-4865-8879-cef3d34812b2" />


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

<img width="332" height="105" alt="Screenshot 2026-07-24 215231" src="https://github.com/user-attachments/assets/f37ca97d-159e-48b1-b2b5-0d005f14c2f3" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="345" height="136" alt="Screenshot 2026-07-24 215251" src="https://github.com/user-attachments/assets/67155760-ea0f-4a1d-bc24-cc19b3334c68" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="375" height="125" alt="Screenshot 2026-07-24 215307" src="https://github.com/user-attachments/assets/7776c474-d3c1-4b4d-b547-1d5753c32560" />

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

<img width="328" height="62" alt="Screenshot 2026-07-24 220051" src="https://github.com/user-attachments/assets/73bca2df-ea95-4b11-825f-9cb2efaae5f1" />


grep hello newfile 
## OUTPUT
<img width="356" height="67" alt="Screenshot 2026-07-24 221025" src="https://github.com/user-attachments/assets/be0bbb7b-62f2-4009-8d04-1e5be03b4854" />




grep -v hello newfile 
## OUTPUT
<img width="336" height="76" alt="Screenshot 2026-07-24 220112" src="https://github.com/user-attachments/assets/a19c740d-5d80-452b-be6a-482429eb1303" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="347" height="86" alt="Screenshot 2026-07-24 220140" src="https://github.com/user-attachments/assets/99b9271d-62a0-4185-bfa8-8ea546e228ac" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="322" height="67" alt="Screenshot 2026-07-24 220209" src="https://github.com/user-attachments/assets/fb4c2349-ff51-4a01-8108-e0be73141b3a" />


grep -R ubuntu /etc
## OUTPUT
<img width="1107" height="267" alt="Screenshot 2026-07-24 220229" src="https://github.com/user-attachments/assets/faa1042e-c391-4e3c-bee2-c30a7bdf455b" />



grep -w -n world newfile   
## OUTPUT
<img width="397" height="88" alt="Screenshot 2026-07-24 220251" src="https://github.com/user-attachments/assets/7848a0f4-bacd-492b-82d6-7b2430b327fc" />


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
<img width="377" height="88" alt="image" src="https://github.com/user-attachments/assets/3e60ef6d-dc0d-4a75-80db-071676005a8a" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="377" height="88" alt="image" src="https://github.com/user-attachments/assets/3e60ef6d-dc0d-4a75-80db-071676005a8a" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="393" height="92" alt="image" src="https://github.com/user-attachments/assets/2ef9ac91-701e-486f-88f3-9b870e0abb4f" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="353" height="67" alt="image" src="https://github.com/user-attachments/assets/71663751-f54b-4d93-a962-826848fef1de" />


egrep '(world$)' newfile 
## OUTPUT
<img width="357" height="83" alt="image" src="https://github.com/user-attachments/assets/135df9e4-7968-49da-8c6e-f1e2bf12566a" />



egrep '(World$)' newfile 
## OUTPUT

<img width="352" height="68" alt="image" src="https://github.com/user-attachments/assets/e7c176fb-c832-45e7-907c-d8ca8e1d4cf1" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="323" height="91" alt="image" src="https://github.com/user-attachments/assets/c63e8922-7cf4-4cc8-872a-0349b56e7c58" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="357" height="77" alt="image" src="https://github.com/user-attachments/assets/b039445d-6234-4ddd-888b-c4366a3b8441" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="337" height="71" alt="image" src="https://github.com/user-attachments/assets/61ad6c72-c6ef-4eb0-b980-b138e7ce7676" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="403" height="63" alt="image" src="https://github.com/user-attachments/assets/efab3988-da15-4540-89fc-9139404c4596" />


egrep l{2} newfile
## OUTPUT
<img width="337" height="92" alt="image" src="https://github.com/user-attachments/assets/fcfb553f-650d-4c21-9c5c-60dd9edd8932" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="400" height="105" alt="image" src="https://github.com/user-attachments/assets/9edd3e41-0e58-42d0-a98d-9706ecb83945" />


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
<img width="353" height="67" alt="image" src="https://github.com/user-attachments/assets/e9628ecb-dac8-4f45-9a42-7af7c48ff9f0" />



sed -n -e '$p' file23
## OUTPUT
<img width="357" height="61" alt="image" src="https://github.com/user-attachments/assets/4c9c3329-ce4e-4e09-bfd6-5dc2c1a8f6c9" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="400" height="231" alt="image" src="https://github.com/user-attachments/assets/006e8a06-3336-4565-a9ce-d0b4f3e4bb82" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="392" height="227" alt="image" src="https://github.com/user-attachments/assets/d5355964-3730-441a-a65a-4b46c83922f6" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="378" height="227" alt="image" src="https://github.com/user-attachments/assets/03553316-06d1-4789-acfd-a550e7a84348" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="346" height="145" alt="image" src="https://github.com/user-attachments/assets/21a6a920-68c2-4f02-8322-8e0c53c49b03" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="370" height="108" alt="image" src="https://github.com/user-attachments/assets/e09fed97-008a-4d3e-9a11-5571f9531832" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

****
<img width="387" height="83" alt="image" src="https://github.com/user-attachments/assets/8c60e2e3-ec8f-44b5-84e6-effc8b418c58" />


seq 10 
## OUTPUT
<img width="392" height="248" alt="image" src="https://github.com/user-attachments/assets/98ddc839-1167-44d7-8e19-e5160515b863" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="346" height="113" alt="image" src="https://github.com/user-attachments/assets/a222c7a1-442d-4877-8b79-24b203f802e2" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="343" height="107" alt="image" src="https://github.com/user-attachments/assets/5a72f53c-205a-417c-b6ca-0c1706129e46" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="322" height="127" alt="image" src="https://github.com/user-attachments/assets/0222d814-d302-4c6c-a7b9-5366a6452457" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="351" height="111" alt="image" src="https://github.com/user-attachments/assets/339268cd-fa7c-4b23-a01b-37f2511fb7ce" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="332" height="105" alt="image" src="https://github.com/user-attachments/assets/523c908b-4719-47d7-93e8-36b2a22c2fb8" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="375" height="101" alt="image" src="https://github.com/user-attachments/assets/8a9025da-63ce-4116-a41d-524875ecf638" />



sed -n '2,4{s/$/*/;p}' file23
<img width="412" height="111" alt="image" src="https://github.com/user-attachments/assets/9034abb8-4f45-41ea-818e-bcece58a292e" />


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
<img width="380" height="141" alt="image" src="https://github.com/user-attachments/assets/f6fcdd2d-6ac4-4f72-9e96-38768d922172" />


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
<img width="350" height="145" alt="image" src="https://github.com/user-attachments/assets/b15f6068-c7c9-40f2-be08-c2071ced64c3" />




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="427" height="222" alt="image" src="https://github.com/user-attachments/assets/410dad6c-0ef8-4421-bf63-811359390b76" />

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
<img width="392" height="128" alt="image" src="https://github.com/user-attachments/assets/2cbfb7cd-416e-4492-a703-fd7ccc208e21" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="457" height="121" alt="image" src="https://github.com/user-attachments/assets/7a4238dd-7137-49dc-bb4a-8607600f148a" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="501" height="527" alt="image" src="https://github.com/user-attachments/assets/3ff7b64e-c38e-4963-99da-f034e014f80b" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="565" height="506" alt="image" src="https://github.com/user-attachments/assets/abb87a59-3318-4bfe-8332-1a8f79ff4921" />


tar -xvf backup.tar
## OUTPUT
<img width="493" height="501" alt="image" src="https://github.com/user-attachments/assets/e5f50cd1-9431-4691-8e8d-60b95177a220" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="528" height="33" alt="image" src="https://github.com/user-attachments/assets/f7b7f8c6-3e59-46ef-a8d8-6040a8f41607" />

gunzip backup.tar.gz
## OUTPUT
<img width="517" height="91" alt="image" src="https://github.com/user-attachments/assets/ee7c96e6-1f35-48e6-9417-7d7cc5772945" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="518" height="63" alt="image" src="https://github.com/user-attachments/assets/82b71ce5-3a6b-4293-b7c3-5fa6138c5255" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="421" height="100" alt="image" src="https://github.com/user-attachments/assets/8dfd41cd-1aa8-49ee-a497-a8509655ef5f" />


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
<img width="518" height="347" alt="image" src="https://github.com/user-attachments/assets/eb65dd62-a785-400f-8045-fbc09086a5ab" />

 
ls file1
## OUTPUT
<img width="482" height="57" alt="image" src="https://github.com/user-attachments/assets/8f1a3710-9669-46c2-9947-94d96dbdd495" />
 
echo $?
## OUTPUT 
 <img width="452" height="63" alt="image" src="https://github.com/user-attachments/assets/4151bf00-7323-4009-a33b-e308df026610" />

abcd
 
echo $?
 ## OUTPUT
<img width="506" height="71" alt="image" src="https://github.com/user-attachments/assets/39936266-bd95-4a85-abf7-692f909bf2dc" />


 
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
<img width="432" height="240" alt="image" src="https://github.com/user-attachments/assets/0bbdf338-4516-4705-9de9-e9a6b1ce74f1" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="555" height="82" alt="image" src="https://github.com/user-attachments/assets/f5db993e-629e-4087-960a-d2a106305e99" />


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
<img width="407" height="57" alt="image" src="https://github.com/user-attachments/assets/556669b4-d65f-4f9a-8d47-b9ba6ebfbc19" />

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
