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


chanchal singhvi c.k. shukla s.n. dasgupta sumit chakrobarty ^d
cat < file2
## OUTPUT
cat > file2

anil aggarwal barun sengupta c.k. shukla lalit chowdury s.n. dasgupta ^d

# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/94bfec13-e94f-4c52-8982-54f52b1cfe12)
comm file1 file2
 ## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/c9cbfcc3-9317-47c3-a258-00ac97fade4d)

diff file1 file2
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/5c72a80b-f0b5-4345-a1f1-e09ff35ae567)


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

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/cf70d1dc-35bc-4b1f-8aa7-575d78fe2f9b)



cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/c986e71a-3adc-4182-bb3c-cc03359426f5)


cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/7bafe0ee-e4fc-459a-912b-c4cc77d99562)


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

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/1f7b83de-17e9-4e44-9d73-021049a1d3f5)


grep hello newfile 
## OUTPUT

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/16a1b74b-e174-44c7-8f7c-356ec9cc659c)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/575b62e6-fc27-44cb-90d9-6167cfb5a46b)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/5157ca11-60fc-48a2-b625-dad0cb54dca4)



cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/cc4810b8-9500-4050-ae8c-47f3f619979b)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/f33c8212-9a93-41e7-bdc7-fdd2960ea00d)



grep -w -n world newfile   
## OUTPUT


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

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/be0b43ec-7a50-447f-bc80-3cc9184c4444)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/317327b4-f3cb-417e-8006-cf1476ccd78f)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/8ef7ee3e-4d0f-4930-bbe4-3ffeaa7f6c78)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/1dba5bec-3696-4d02-9ffa-eac2635140c9)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/54f89276-46a9-4a9b-bb35-e1cd007d44e9)


egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/fa97dd22-91b7-4678-b879-889a25b74fe3)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/90a7e2b0-a67e-434b-aac7-06e70cb81b74)



egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/94075e05-56f7-409c-a386-9ac6bf3a4e11)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/871e0675-d8f0-454d-ae5d-fc216c836d34)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/f80ee10d-08f3-4ee7-a1d8-151974460873)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/724be14b-fee0-4d11-8c12-ab6352c054fb)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/0cdb8c0e-4502-41ee-a5ed-dbc951e95478)


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

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/ee7e649b-a181-4a94-bf9f-6ddd1d0320a7)


sed -n -e '$p' file23
## OUTPUT


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/d902cfd7-9058-4dc2-9794-7f5c964d467a)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/c1245400-1c15-438f-9262-014ebb02a494)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/7d8a39dc-b986-413c-aea3-e6aa8f6a3b88)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/b38bb1de-5f27-4f21-82b1-347fa44e39e8)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/705b2fa9-67de-41eb-998b-77f2b28d1737)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/bb39b8a3-5017-47d8-a4c8-8abf2a81e48c)



seq 10 
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/c9e9be83-2ab7-43cd-a2be-03ba6179a3d5)



seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/d796915f-c36a-4696-8168-8cf05d926a1d)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/fa7f8def-d991-4c53-bbf6-fd56c96f8c6e)


seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/f98fa41e-5309-4273-b279-fac468534109)


seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/e7b8b3ea-deb3-410f-bcf8-46e40370951b)


seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/065e9771-d637-4d98-82d6-bb8d3083bc77)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/76ff5ba0-e8e5-43d8-bf19-eea647a393f3)



sed -n '2,4{s/$/*/;p}' file23
# OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/04985d3e-5395-4de6-ba77-6cd8d79683c5)


# Sorting File content
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
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/2040fb18-d12b-4bdc-9895-30f2089baca5)


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

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/69ae654c-f387-44c8-baab-723896943e7a)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/e1418a27-5746-417f-b530-38f07ebc2ad3)

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

![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/c6562169-557a-43f5-a62d-e6325f40a265)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/6a1659e9-cc40-4a2d-887b-e882275a2d65)



# Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/BharathCSEIOT/OS-Linux-commands-Shell-script/assets/122793480/026082f8-fb8b-47e4-817f-81503e57b8a7)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

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


cat < scriptest.sh 
```
bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
@@ -425,10 +476,10 @@ echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
@@ -440,37 +491,28 @@ echo 'The $@ is ' $@
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
```
bash
\#!/bin/bash
val1=baseball
val2=hockey
@@ -481,10 +523,10 @@ else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
@@ -494,20 +536,15 @@ echo "$val1 is greater than $val2"
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
```
bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
@@ -516,24 +553,23 @@ else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```
bash
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
```
bash
\#!/bin/bash
if [ -e $HOME ]
then
@@ -552,9 +588,9 @@ else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
@@ -572,16 +608,13 @@ fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT



# using numeric test comparisons
cat > iftest.sh 
```
bash
\#!/bin/bash
val1=10
val2=11
@@ -596,11 +629,11 @@ else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```
bash
\#!/bin/bash
val1=10
val2=11
@@ -614,16 +647,15 @@ echo “The values are equal”
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
@@ -642,10 +674,10 @@ else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```
bash
\#!/bin/bash
if [ -e $HOME ]
then
@@ -663,16 +695,14 @@ fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh 
```
bash
\#!/bin/bash
if [ $USER = Ram ]
then
@@ -691,32 +721,28 @@ echo "$USER, Do not forget to logout when you're done"
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
```
bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
@@ -728,13 +754,11 @@ echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```
bash
#!/bin/bash
#while command test
var1=10
@@ -743,97 +767,97 @@ do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```
bash
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
```
bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
@@ -885,15 +909,13 @@ do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

 
cat forbreak.sh 
```
bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
@@ -905,15 +927,14 @@ fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```
bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
@@ -925,46 +946,44 @@ fi
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
```
bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
@@ -977,29 +996,25 @@ echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```
bash
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
``` 
bash
#num=545
echo "Enter the number"
read num
@@ -1083,9 +1095,7 @@ then
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 


# RESULT:
The Commands are executed successfully.
