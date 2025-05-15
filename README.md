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

![Screenshot from 2025-04-28 13-25-24](https://github.com/user-attachments/assets/fd1761ad-3790-489f-80b4-7bee08baec2c)

cat < file2
## OUTPUT

![Screenshot from 2025-04-28 13-25-39](https://github.com/user-attachments/assets/1892f972-7a6c-466e-b6af-4ec2e47cc0ed)



# Comparing Files
cmp file1 file2
## OUTPUT

![Screenshot from 2025-04-28 13-26-36](https://github.com/user-attachments/assets/1aeb97fd-83fe-4262-8627-a60ed0c21335)

comm file1 file2
 ## OUTPUT

![Screenshot from 2025-04-28 13-27-19](https://github.com/user-attachments/assets/eea52ae9-fc7a-4964-8b9b-3b63e1d4b198)

diff file1 file2
## OUTPUT

![Screenshot from 2025-04-28 13-27-55](https://github.com/user-attachments/assets/a2490056-93ad-4fa0-b203-7e9b15b7a338)



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

![Screenshot from 2025-04-28 13-33-13](https://github.com/user-attachments/assets/8f1eadb6-30ea-4a78-8a7f-76247ec64ec2)




cut -d "|" -f 1 file22
## OUTPUT

![Screenshot from 2025-04-28 13-34-30](https://github.com/user-attachments/assets/95e27206-d3d7-47da-8f8c-5983c8de7d9e)


cut -d "|" -f 2 file22
## OUTPUT

![Screenshot from 2025-04-28 13-35-29](https://github.com/user-attachments/assets/22df0f1e-b3c5-4188-92a6-0ac66a2a29f7)


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


![Screenshot from 2025-04-28 13-39-49](https://github.com/user-attachments/assets/7754ddfe-5551-4f3c-9f8c-4d24922f09f6)

grep hello newfile 
## OUTPUT

![Screenshot from 2025-04-28 13-40-27](https://github.com/user-attachments/assets/59b49474-858d-4b31-b7a6-e65c271e8c12)



grep -v hello newfile 
## OUTPUT

![Screenshot from 2025-04-28 13-40-53](https://github.com/user-attachments/assets/e71a9461-9f47-4336-9b98-ba1377fd14bb)



cat newfile | grep -i "hello"
## OUTPUT


![Screenshot from 2025-04-28 13-42-51](https://github.com/user-attachments/assets/9f6e5058-dfcb-4411-a0f4-681e6d3e399e)


cat newfile | grep -i -c "hello"
## OUTPUT


![Screenshot from 2025-04-28 13-43-37](https://github.com/user-attachments/assets/cd3368c8-f37c-46db-80c4-375668005cb1)


grep -w -n world newfile   
## OUTPUT

![Screenshot from 2025-04-28 13-44-12](https://github.com/user-attachments/assets/1d15b9a1-e84b-4e3d-b62b-3631c3a2aeee)

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


![Screenshot from 2025-04-28 13-50-09](https://github.com/user-attachments/assets/52aca5de-81a5-4858-9af3-9c45893b9344)


egrep -w '(H|h)ello' newfile 
## OUTPUT


![Screenshot from 2025-04-28 13-51-16](https://github.com/user-attachments/assets/bb2bd03e-8261-4e72-8cfe-cc0d2ab3e0e7)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![Screenshot from 2025-04-28 13-52-16](https://github.com/user-attachments/assets/68295d77-e992-4ce2-b5f4-7a22ffda9fda)



egrep '(^hello)' newfile 
## OUTPUT


![Screenshot from 2025-04-28 13-52-57](https://github.com/user-attachments/assets/884a0c7f-5e7c-4ce7-9aea-a5f5b11b18a7)


egrep '(world$)' newfile 
## OUTPUT

![Screenshot from 2025-04-28 13-53-37](https://github.com/user-attachments/assets/5858954c-3f17-4203-a9c5-d849d377ced9)


egrep '(World$)' newfile 
## OUTPUT


egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot from 2025-04-28 13-55-23](https://github.com/user-attachments/assets/5f8e8eb2-7b31-4b43-88e4-f66f60219bcb)



egrep '[1-9]' newfile 
## OUTPUT

![Screenshot from 2025-04-28 13-58-39](https://github.com/user-attachments/assets/abc96c0d-e91c-48ce-b281-54f994b051c2)



egrep 'Linux.*world' newfile 
## OUTPUT

![Screenshot from 2025-04-28 13-59-56](https://github.com/user-attachments/assets/b66f589f-6f35-4d43-bb54-8cf8fffd8185)


egrep 'Linux.*World' newfile 
## OUTPUT

![Screenshot from 2025-04-28 14-00-44](https://github.com/user-attachments/assets/d59c890b-e1bd-41d5-948d-c1e2bcc39824)








egrep 's{1,2}' newfile
## OUTPUT 

![Screenshot from 2025-04-28 14-01-25](https://github.com/user-attachments/assets/6c82dbc3-d76f-4a9b-ac46-d968e8946ab1)



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


![Screenshot from 2025-04-28 14-06-04](https://github.com/user-attachments/assets/6bbf88b9-378c-49d7-b269-691609215fac)


sed -n -e '$p' file23
## OUTPUT


![Screenshot from 2025-04-28 14-06-47](https://github.com/user-attachments/assets/fe2c7bc4-ad39-4e42-a068-b186835030a5)

sed  -e 's/Ram/Sita/' file23
## OUTPUT


![Screenshot from 2025-04-28 14-07-27](https://github.com/user-attachments/assets/965960b8-37dd-473e-91d6-500ec25e6766)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-04-28 14-08-11](https://github.com/user-attachments/assets/4f2dcce3-004c-420f-8f25-fa329aee78e6)



sed  '/tom/s/5000/6000/' file23
## OUTPUT


![Screenshot from 2025-04-28 14-08-44](https://github.com/user-attachments/assets/f6638d8d-5251-44a8-832b-abc889dcf76d)


sed -n -e '1,5p' file23
## OUTPUT

![Screenshot from 2025-04-28 14-09-22](https://github.com/user-attachments/assets/1171fab7-f939-46fa-b46a-89090a2db9f4)



sed -n -e '2,/Joe/p' file23
## OUTPUT


![Screenshot from 2025-04-28 14-10-02](https://github.com/user-attachments/assets/49755259-f7aa-4464-9d61-28bbdb0677af)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-04-28 14-10-45](https://github.com/user-attachments/assets/864979c3-3385-4a02-9e2b-c939a6bc904b)


seq 10 
## OUTPUT


![Screenshot from 2025-04-28 14-11-03](https://github.com/user-attachments/assets/e23173ba-f85b-4dde-978d-5c6b050fda18)


seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot from 2025-04-28 14-11-42](https://github.com/user-attachments/assets/9935e74c-bdf2-4355-89ac-9b8d503cacb4)



seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot from 2025-04-28 14-12-20](https://github.com/user-attachments/assets/35580db1-e539-4700-b906-90f196b60250)



seq 3 | sed '2a hello'
## OUTPUT

![Screenshot from 2025-04-28 14-12-50](https://github.com/user-attachments/assets/dc6b1797-88a6-4b2b-8b9f-5410556ba590)



seq 2 | sed '2i hello'
## OUTPUT

![Screenshot from 2025-04-28 14-13-21](https://github.com/user-attachments/assets/b8e108e0-bd2e-4297-a59d-cb1bd8041d17)


seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot from 2025-04-28 14-13-53](https://github.com/user-attachments/assets/dbc85c5e-1aab-4846-b862-1491b488dfcb)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot from 2025-04-28 14-14-37](https://github.com/user-attachments/assets/c18f7eda-dc70-4774-8ba7-c8398a4acb06)



sed -n '2,4{s/$/*/;p}' file23


![Screenshot from 2025-04-28 14-16-12](https://github.com/user-attachments/assets/ad4a4671-28e8-4f18-80dd-4ddf0b8ca462)

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

![Screenshot from 2025-04-28 14-19-47](https://github.com/user-attachments/assets/aa02c7e2-6b29-4c7b-b3c4-3aaa2e0650ca)


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


![Screenshot from 2025-04-28 14-22-52](https://github.com/user-attachments/assets/c4a52a33-8a4a-479f-9289-4c78be74da3c)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT


![Screenshot from 2025-04-28 14-23-40](https://github.com/user-attachments/assets/fc62799a-35f2-42f6-9c83-8c9ffce2ddbf)

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

![Screenshot from 2025-04-28 14-28-11](https://github.com/user-attachments/assets/6b9961bd-4c9b-4d16-8b12-5deb08f5f905)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


![Screenshot from 2025-04-28 14-29-06](https://github.com/user-attachments/assets/50fd1623-5ec5-406d-85ec-30b4c2a1daea)



#Backup commands
tar -cvf backup.tar *
## OUTPUT

![Screenshot from 2025-04-28 14-32-03](https://github.com/user-attachments/assets/79854d76-1caf-49d8-bdd3-6f70bcd0d5ab)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/b090597c-0ecd-419f-a678-1ffb97768c94)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/1b40b14d-9db7-4c77-b36d-c850d4e1fc36)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/user-attachments/assets/a7eadb43-e5b0-4ac1-9762-57787e6d65c9)

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
![image](https://github.com/user-attachments/assets/20f417a4-d03e-420e-8509-3f7d4d02c93a)


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
