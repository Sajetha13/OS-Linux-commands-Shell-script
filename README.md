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
![file1](/img/file1.png)

cat < file2
## OUTPUT
![file2](/img/file2.png)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![cmp](/img/cmp.png)

comm file1 file2
 ## OUTPUT
![comm](/img/comm.png)
 
diff file1 file2
## OUTPUT
![diff](/img/diff.png)

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
![image](https://github.com/user-attachments/assets/b1df05de-cb5d-4fa8-be91-08eda9bb599e)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/9f10d132-6fe3-40aa-ad46-aa7a99cde14c)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/2803873f-1316-4db8-836c-343e6d0b5ab9)


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
![image](https://github.com/user-attachments/assets/da65e121-275e-49b5-91b4-2b80f1257e3f)



grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/c0fcceb9-5f6a-4bbb-8898-e95dee9e1a71)



grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/8a4c6d8d-24f6-4b51-a91c-34bed0de398d)



cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/2fe19af7-906f-4e0e-b0f1-ac48649ef92f)



cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/f32950fd-c6dd-408f-a0ee-436bd0a36571)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/cdf1119d-0200-4fdf-8ad6-a065b31d5c6f)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/912072a4-932c-4732-b7ee-23839a738400)


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
![image](https://github.com/user-attachments/assets/7041c7d7-f9aa-4315-9151-30296e5a04ce)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/38d614ef-3eb5-4444-a3af-ebe80e5968cd)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/d0902c03-1bcd-4fea-ac48-4eb5d2d2c2ab)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/83dc4813-ebf6-4b07-8a6d-9d12de0499ab)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/6f0fbd4d-48bc-47a3-b213-45796d6c125f)


egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/00e7d001-b5f3-4522-a7bb-af7f02772fdb)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/83be4137-e76a-422c-891c-3715c6ca0d5a)



egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/b2d3014b-7b6c-4618-9327-688803afc5e3)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/c01f1025-0e4b-436b-a3b8-08e446fcaa6a)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/98313656-2416-4120-918b-5e24b097d37b)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/ec45457c-511a-49b1-ac8f-1f1f5c13917a)


egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/977a24f7-9f53-47af-8e03-4f3daff0dec2)


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
![image](https://github.com/user-attachments/assets/7b3b811b-6922-46c5-b0a0-3add380701c8)



sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/52380905-d782-4518-8e35-4e63287bd04f)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/73979d4e-0d5f-429d-bc2c-8f6668e4f954)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/47588f7e-cf00-4c6e-b127-27b263c3fbeb)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/804f1c8d-681f-47b5-b21c-d4451a7aae10)


sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/2cd1aa4a-8f8f-4665-9597-85f2c362cf71)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/8dd077ee-ac00-44d1-9b46-bd04b329f704)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/b7a9f2bb-ce3b-49ed-8125-509ab7f24795)


seq 10 
## OUTPUT



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/89cb0cab-b1d7-441e-9f95-324b220fdacf)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/b9bc6d4c-3fc6-4c4e-a2a4-eea75ecaf5cf)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/1e590fd8-0717-4804-a527-6e9736b4e560)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/e974509a-d94c-4eea-9b26-6b897bfbb832)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/5666cf8a-f2f5-42eb-b039-5c9660583b27)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/450eb934-6efa-4cf4-b251-1689a8726cba)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/62702896-0f62-4661-a305-a37d35797ca4)


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
![Screenshot 2024-09-10 133403](https://github.com/user-attachments/assets/2d17719b-a607-4bc7-9c9a-8eb4cf380402)


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
![Screenshot 2024-09-10 133426](https://github.com/user-attachments/assets/53b7be8d-2884-4362-ba6b-6972f0241233)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot 2024-09-10 133320](https://github.com/user-attachments/assets/08548ed0-4662-41fb-a965-bfce97b9d58c)

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
![Screenshot 2024-09-10 133802](https://github.com/user-attachments/assets/6854ccfc-dc45-4e1a-abc8-193b36a5c195)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot 2024-09-10 133744](https://github.com/user-attachments/assets/c720587d-c38a-4f46-a5b9-664b10837127)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![Screenshot 2024-09-10 133724](https://github.com/user-attachments/assets/a9bf0aa3-4354-4591-9e44-9fae8a472a53)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/d9d09d49-79d3-4df4-bab2-4b57a9aede59)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/448eceac-de1c-4833-9e92-9aaa091dd2c1)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/user-attachments/assets/f4a4da3a-9262-4285-b2e1-e0ce9a3a3f16)

gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/5ca72276-29e6-46f1-87e3-5c6eaaf3b028)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/f84fbc68-2fa5-48e3-b119-2cf80bb25663)


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
![image](https://github.com/user-attachments/assets/448b8899-b68a-4478-a9ca-a850dd50f222)

 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/4f709d5a-89df-4081-870a-9efb89f6f408)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/5771ef9f-e330-4b95-8101-bc447506ed1b)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![image](https://github.com/user-attachments/assets/e268979f-ada2-451e-8404-012dca5e72d9)

abcd
 
echo $?
 ## OUTPUT


 ![image](https://github.com/user-attachments/assets/d0b9bf89-f848-483b-8212-ef93c3594c2b)

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
## OUTPUT
![image](https://github.com/user-attachments/assets/7c283d88-aeca-403f-9fad-4e54c7755432)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/4abd3ebb-b148-4742-ac46-5092fb4cb57e)

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
![image](https://github.com/user-attachments/assets/ba33f203-538a-421d-b6c6-df69e3de7db1)

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

![image](https://github.com/user-attachments/assets/dd1424b1-2416-4a78-8da7-6c9482746955)


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
![image](https://github.com/user-attachments/assets/1720c083-1cba-46d8-877b-7127986ee13c)

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
![image](https://github.com/user-attachments/assets/6395c4b7-cac7-4740-838a-6d33c9ba2983)

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
![image](https://github.com/user-attachments/assets/47bbf9c2-1a68-415d-99ed-9428138c3e17)


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
![image](https://github.com/user-attachments/assets/f5c0c01e-b35a-4a51-908a-9795cbb17149)

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
![image](https://github.com/user-attachments/assets/ba219456-e34d-46cd-9cf5-27ab8fb2977c)

 
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
 ![image](https://github.com/user-attachments/assets/5674f61b-c849-4748-aa28-1419af6e9b01)

 
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
 
 ![image](https://github.com/user-attachments/assets/07328cfd-dde9-4524-a86c-6a5894c309f8)

 
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
 ![image](https://github.com/user-attachments/assets/4b5f1e78-8247-4cb9-8263-6921180e4085)

 
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
 ![image](https://github.com/user-attachments/assets/6e88d24c-b494-4d7a-af50-8ac80b042bf6)


 
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
 ![image](https://github.com/user-attachments/assets/59ad5c4c-0bd3-4855-8d21-8d9dcba7e063)

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
![image](https://github.com/user-attachments/assets/e2cd30d0-a90c-4e73-af97-46a1fba5e713)

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype1.sh
$ ./forctype1.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/d93aab9b-1d4a-4ea0-be8d-1e110554317e)

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
![image](https://github.com/user-attachments/assets/0cb94f3b-f2dc-4eb3-a18f-4ed866ca7e08)

 
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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
## OUTPUT
 ![image](https://github.com/user-attachments/assets/992d70ac-290c-4b57-b366-031600d2d9ab)

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

 
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
## OUTPUT
 ![image](https://github.com/user-attachments/assets/e4d7b54b-1130-4cb5-99e6-0596413267fc)

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
![image](https://github.com/user-attachments/assets/3fd572ea-58be-46cf-818b-e2234d9fa99b)


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
![image](https://github.com/user-attachments/assets/0d4474c3-8c55-427a-bcf8-b2f36fe17231)




 
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

 ![image](https://github.com/user-attachments/assets/28713a0b-050f-49c4-abcc-060e1eb9d085)

 ./funcex.sh 1 2
![image](https://github.com/user-attachments/assets/537cc739-f609-4af7-8dcc-3a2e44278930)

 
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
 ![image](https://github.com/user-attachments/assets/2a00f75b-77a4-4194-8592-e6cb6e9e4db7)

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
 ![image](https://github.com/user-attachments/assets/ae81e9f5-344d-4868-95b8-bb5abf83d615)

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
 ![image](https://github.com/user-attachments/assets/e4d3d73f-983e-4b74-936d-a280d9f6aad4)

 
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
 ![image](https://github.com/user-attachments/assets/9a8f7006-7559-4e77-b4d8-c26ade89cda0)

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

![image](https://github.com/user-attachments/assets/64645861-adc2-4a2b-8bf6-0e9dba3b860a)

# RESULT:
The Commands are executed successfully.
