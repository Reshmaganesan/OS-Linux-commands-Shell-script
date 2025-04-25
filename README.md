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

![Screenshot from 2025-04-25 18-01-48](https://github.com/user-attachments/assets/721ad051-afe5-4a54-8b5d-21bfab90c476)


cat < file2
## OUTPUT


![Screenshot from 2025-04-25 18-05-34](https://github.com/user-attachments/assets/cfa7e2a6-4eb9-4f23-b604-f2ea2b3ad0b2)

# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot from 2025-04-25 18-07-21](https://github.com/user-attachments/assets/4c60f0f3-7816-4b5f-b0d4-3191f0fa3f24)

 
comm file1 file2
 ## OUTPUT

 ![Screenshot from 2025-04-25 18-17-35](https://github.com/user-attachments/assets/0c62afae-ea8c-41bb-b8f9-fcd44802ff0c)


 
diff file1 file2
## OUTPUT

![Screenshot from 2025-04-25 18-18-44](https://github.com/user-attachments/assets/2c6fed59-af23-4b04-92eb-cf8adec3eb98)



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
![Screenshot from 2025-04-25 18-25-18](https://github.com/user-attachments/assets/7536cfb8-3643-4121-b40e-803d9bfa52d1)





cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-04-25 18-26-22](https://github.com/user-attachments/assets/2082714f-f5a2-4a3a-b371-0ad0ea1e7ae1)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-04-25 18-26-00](https://github.com/user-attachments/assets/2a86863f-4488-4bc6-a21d-b0c91cccf1d3)



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
![Screenshot from 2025-04-25 18-30-37](https://github.com/user-attachments/assets/2bef7332-8892-424c-b7cf-0955b449aa39)



grep hello newfile 
## OUTPUT
![Screenshot from 2025-04-25 18-31-07](https://github.com/user-attachments/assets/dfd6f6c4-2569-4dcc-9945-234dcfe8218a)




grep -v hello newfile 
## OUTPUT

![Screenshot from 2025-04-25 18-32-26](https://github.com/user-attachments/assets/fe579575-f224-409e-87f1-6ac2d87c9bd0)


cat newfile | grep -i "hello"
## OUTPUT

![Screenshot from 2025-04-25 18-33-28](https://github.com/user-attachments/assets/e07a628a-bd95-443c-8c54-40b45f91698a)



cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot from 2025-04-25 18-34-56](https://github.com/user-attachments/assets/4c3327f0-d1c1-4e21-80ae-3063eccaa3bf)



grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2025-04-25 18-35-51](https://github.com/user-attachments/assets/53181e8b-dee1-4227-b544-72f926351e87)




grep -w -n world newfile   
## OUTPUT

![Screenshot from 2025-04-25 18-38-55](https://github.com/user-attachments/assets/8ab15022-b319-4307-82f5-90417cc096da)




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

![Screenshot from 2025-04-25 18-44-13](https://github.com/user-attachments/assets/a28fee6b-9249-4782-8280-800b7fcb7747)




egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2025-04-25 18-45-52](https://github.com/user-attachments/assets/6cbaf758-e4fa-4f33-9571-ce24b3c402a3)




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot from 2025-04-25 18-47-18](https://github.com/user-attachments/assets/07fde99c-fa6e-43f6-8542-b9d824c158bb)




egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2025-04-25 18-48-39](https://github.com/user-attachments/assets/4b2c8ff3-3f3d-4473-a0cd-f477d455a302)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2025-04-25 18-53-51](https://github.com/user-attachments/assets/fa2ad97d-7d82-45ba-97bf-e1d23ae701f5)




egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-04-25 18-54-36](https://github.com/user-attachments/assets/5b9cc1f3-f494-4c0c-9def-1cc8329fe00e)



egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2025-04-25 18-55-26](https://github.com/user-attachments/assets/7a3fdebf-ef28-4cd2-9ca1-b058ec7af2ec)



egrep '[1-9]' newfile 
## OUTPUT

![Screenshot from 2025-04-25 18-56-22](https://github.com/user-attachments/assets/4a0bc97d-37be-4afd-9684-9fcac1cca4ab)


egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-04-25 18-57-27](https://github.com/user-attachments/assets/19deb4ab-a55f-4b46-8054-1483263edb39)


egrep 'Linux.*World' newfile 
## OUTPUT

![Screenshot from 2025-04-25 18-58-21](https://github.com/user-attachments/assets/e2c97bd5-e6d9-45b0-81fa-ce21f0eb3dce)

egrep l{2} newfile
## OUTPUT
![Screenshot from 2025-04-25 18-59-20](https://github.com/user-attachments/assets/a7bbff59-c6b2-4669-970f-5e3d85632980)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2025-04-25 19-00-00](https://github.com/user-attachments/assets/b6fe9251-3cce-4fef-9b35-5e381541c7d8)



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
![Screenshot from 2025-04-25 19-02-20](https://github.com/user-attachments/assets/97428970-d632-46d1-8a9d-a7b017ee9688)




sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2025-04-25 19-03-16](https://github.com/user-attachments/assets/422c8115-4540-4646-822f-2f95972ca791)





sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-04-25 19-04-38](https://github.com/user-attachments/assets/4bafcc98-35b0-45ca-bba6-679c11aa1533)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-04-25 19-06-17](https://github.com/user-attachments/assets/76ed1d29-1f08-497b-8a65-7e1ca53995d6)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2025-04-25 19-07-08](https://github.com/user-attachments/assets/c518afcd-8113-458f-8bb4-2c47bc5fdc45)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2025-04-25 19-07-50](https://github.com/user-attachments/assets/742c6ed6-99c1-43b0-a449-ac3b85dffaaa)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-04-25 19-08-48](https://github.com/user-attachments/assets/9f4ebf05-0f97-4fbc-a1b2-6756aab26c2a)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-04-25 19-09-47](https://github.com/user-attachments/assets/a4294f8b-e6ac-43a1-a79d-dc122ef23bf8)



seq 10 
## OUTPUT
![Screenshot from 2025-04-25 19-10-27](https://github.com/user-attachments/assets/4af21a6f-2a07-4f3d-b7bd-5baa5ca20bf5)




seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2025-04-25 19-11-28](https://github.com/user-attachments/assets/9ca7375c-9883-46aa-ab2a-d792191d24cd)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2025-04-25 19-13-00](https://github.com/user-attachments/assets/5ed0c3d0-c4f0-404f-b925-2773ae6c304d)




seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2025-04-25 19-14-41](https://github.com/user-attachments/assets/a0f9235c-1d79-489e-98f5-974efcc18bd9)




seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2025-04-25 19-16-17](https://github.com/user-attachments/assets/fc18ac83-d38c-4510-a257-32f1df93326a)



seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2025-04-25 19-16-51](https://github.com/user-attachments/assets/fccecb40-18e5-401f-ad1a-901f446b504b)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2025-04-25 19-18-30](https://github.com/user-attachments/assets/741a6736-4a9e-4ca2-9838-d1d1bbe86dae)




sed -n '2,4{s/$/*/;p}' file23


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
![Screenshot from 2025-04-25 19-27-47](https://github.com/user-attachments/assets/e7403b51-e907-4ae3-bd40-69a429b9345a)



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
![Screenshot from 2025-04-25 19-31-24](https://github.com/user-attachments/assets/3c357efd-c52c-4cd7-b996-4626a3db501b)




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 ![Screenshot from 2025-04-25 19-33-00](https://github.com/user-attachments/assets/66b1daa9-9853-48ac-9876-3e8710f07787)


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
 ![Screenshot from 2025-04-25 19-37-23](https://github.com/user-attachments/assets/fb2e0421-a44a-4b84-ad07-7d8aff66374d)



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot from 2025-04-25 19-38-37](https://github.com/user-attachments/assets/d1bbd6b9-fa28-46ab-bfbc-04c12bb9c564)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2025-04-25 19-39-15](https://github.com/user-attachments/assets/6e432bb3-965f-4d71-a8de-2f2e387127ed)


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
