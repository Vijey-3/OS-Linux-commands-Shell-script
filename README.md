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

![Screenshot from 2024-09-18 21-42-04](https://github.com/user-attachments/assets/c604bde8-2711-4256-b406-18248740ff26)




cat < file2
## OUTPUT
![Screenshot from 2024-09-18 21-43-31](https://github.com/user-attachments/assets/94d5810f-e093-415f-bad5-ef3ada95ba1e)


# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot from 2024-09-18 21-45-09](https://github.com/user-attachments/assets/6ba667b5-6758-41f9-b577-4a1a24f16b36)


 
comm file1 file2
 ## OUTPUT
![Screenshot from 2024-09-18 21-46-01](https://github.com/user-attachments/assets/f8516b69-6f27-44bf-b6c5-fcceb0a00c8f)

 
diff file1 file2
## OUTPUT
![Screenshot from 2024-09-18 21-46-37](https://github.com/user-attachments/assets/3b226bb9-f3cd-48f5-80ea-e65a0a269c12)


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

![Screenshot from 2024-09-18 21-48-11](https://github.com/user-attachments/assets/07ec2439-22c9-45c4-9037-6d2b7edda091)



cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2024-09-18 21-48-44](https://github.com/user-attachments/assets/3042ad63-eb8a-4ea6-97a7-fe0264b35ecd)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2024-09-18 21-50-47](https://github.com/user-attachments/assets/b9c7ba85-343c-437e-9362-800fce751d62)


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
![Screenshot from 2024-09-18 21-52-53](https://github.com/user-attachments/assets/ad2cb526-3a78-4ebf-b8c5-a85207385bb0)



grep hello newfile 
## OUTPUT
![Screenshot from 2024-09-18 21-53-25](https://github.com/user-attachments/assets/f3dd4211-6b56-4cfc-b012-6cdc3edb0b6d)




grep -v hello newfile 
## OUTPUT
![Screenshot from 2024-09-18 21-54-44](https://github.com/user-attachments/assets/888586b8-a224-438c-91a8-21ed05b968b7)



cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2024-09-18 21-55-08](https://github.com/user-attachments/assets/fa3b1487-fea9-441b-af67-aa0f4cae0923)




cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot from 2024-09-18 21-55-26](https://github.com/user-attachments/assets/b1d72913-e108-49d3-b671-eee7e62ca917)



grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2024-09-18 21-56-09](https://github.com/user-attachments/assets/2e996756-56db-4c24-af8e-c5ac2a1c0324)



grep -w -n world newfile   
## OUTPUT
![Screenshot from 2024-09-18 21-57-00](https://github.com/user-attachments/assets/daeb6b91-f2e1-46f1-80a1-4a04e8852a85)


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
![Screenshot from 2024-09-18 21-57-46](https://github.com/user-attachments/assets/f2bd26b0-7004-4c5b-8ae1-5b267505924f)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2024-09-18 21-57-59](https://github.com/user-attachments/assets/58a28352-cc0d-48a6-a9ec-02373b452ca4)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot from 2024-09-18 21-58-09](https://github.com/user-attachments/assets/35de4f01-7e3e-404e-b9c4-d0c19a6ded83)




egrep '(^hello)' newfile 
## OUTPUT

![Screenshot from 2024-09-18 21-58-27](https://github.com/user-attachments/assets/16277ba6-e9fc-43e6-abe7-35d8ecc93225)


egrep '(world$)' newfile 
## OUTPUT

![Screenshot from 2024-09-18 21-58-40](https://github.com/user-attachments/assets/4c2aae71-024e-46db-93dc-07869d76b6f8)


egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2024-09-18 21-58-52](https://github.com/user-attachments/assets/3a5944b6-2a74-41ff-92a5-b86efdbf6cf6)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot from 2024-09-18 21-59-04](https://github.com/user-attachments/assets/bb6f95c1-6bcf-4c8e-a656-b76ef30aae9a)


egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2024-09-18 21-59-04](https://github.com/user-attachments/assets/264bf0fb-60a3-4e7d-805f-7841b06bc84c)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2024-09-18 21-59-25](https://github.com/user-attachments/assets/76a67ad0-b0c1-4720-ab89-d4540f5fc4c3)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2024-09-18 21-59-32](https://github.com/user-attachments/assets/cf067e1f-18f7-4f26-992b-b13ac944ed4d)


egrep l{2} newfile
## OUTPUT
![Screenshot from 2024-09-18 21-59-43](https://github.com/user-attachments/assets/74018ac6-70cf-4102-8856-ba03723cd394)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2024-09-18 21-59-55](https://github.com/user-attachments/assets/3068676a-47a3-4990-96dc-a8043f1cea6b)


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

![Screenshot from 2024-09-18 22-00-25](https://github.com/user-attachments/assets/b9dc450c-036c-4d29-b318-d75783920758)


sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2024-09-18 22-00-34](https://github.com/user-attachments/assets/71288d2c-ce9b-42c3-a08c-802d6fc13fc5)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2024-09-18 22-00-44](https://github.com/user-attachments/assets/8093af1a-8482-4177-8646-fb194c8bf417)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2024-09-18 22-00-52](https://github.com/user-attachments/assets/a9371fd3-043d-4e2b-99cb-031cf0b5dd65)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot from 2024-09-18 22-00-59](https://github.com/user-attachments/assets/066b0df1-82c6-4f94-8062-d2224ce7fe41)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2024-09-18 22-01-09](https://github.com/user-attachments/assets/da5c23d3-2f09-4f33-a8dc-03e766bd0734)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot from 2024-09-18 22-01-09](https://github.com/user-attachments/assets/40a3335a-dcce-40ae-bea7-3664572520a1)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2024-09-18 22-01-58](https://github.com/user-attachments/assets/e7883d89-b2f0-44d3-91ff-0094bc4c323f)



seq 10 
## OUTPUT

![Screenshot from 2024-09-18 22-02-18](https://github.com/user-attachments/assets/fffbbba1-e6ef-442d-af0e-0c52c9dbc494)


seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2024-09-18 22-02-29](https://github.com/user-attachments/assets/0fb63d7f-d3b3-48aa-af99-a89e52b54eff)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2024-09-18 22-02-37](https://github.com/user-attachments/assets/f196c91a-37f9-42ae-8b18-90de91d14afb)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2024-09-18 22-02-50](https://github.com/user-attachments/assets/4ee2292b-800e-4d15-9bb0-8a35337d186b)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2024-09-18 22-03-00](https://github.com/user-attachments/assets/33773d14-7416-402a-81cf-61f08cfb6c85)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2024-09-18 22-03-11](https://github.com/user-attachments/assets/dce3c374-6272-4a71-9e6a-80ca3dd77ee8)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2024-09-18 22-03-20](https://github.com/user-attachments/assets/03073051-96d1-42d4-aee1-2c593ebf12c2)



sed -n '2,4{s/$/*/;p}' file23
![Screenshot from 2024-09-18 22-03-28](https://github.com/user-attachments/assets/d9a29fbf-eef7-48f8-bfe7-29b0157e20aa)


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

![Screenshot from 2024-09-18 22-04-32](https://github.com/user-attachments/assets/47e70001-6d80-4c55-af3e-336528aa8daf)

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
![Screenshot from 2024-09-18 22-05-15](https://github.com/user-attachments/assets/fafcf1a3-4601-4e9c-9f8c-edbcf2654c9b)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2024-09-18 22-05-47](https://github.com/user-attachments/assets/154b7f2a-202e-4f5d-be89-089bf3c29eec)

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
![Screenshot from 2024-09-18 22-07-04](https://github.com/user-attachments/assets/93dd6202-d930-4020-967c-7a81dcec7185)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2024-09-18 22-07-11](https://github.com/user-attachments/assets/0551aa7d-d443-4f8c-80c2-75bf86b414c7)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2024-09-18 22-07-27](https://github.com/user-attachments/assets/091d459b-325e-47e1-b9c6-1428fea49c01)


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
