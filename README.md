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
cat < file2

## OUTPUT
<img width="498" height="549" alt="Screenshot (66)" src="https://github.com/user-attachments/assets/21713dde-c859-4570-a17d-abe860cf4d2f" />


# Comparing Files

cmp file1 file2
comm file1 file2
diff file1 file2

## OUTPUT
<img width="522" height="504" alt="Screenshot (67)" src="https://github.com/user-attachments/assets/518a9b39-dcbf-4537-bde8-e584b57f61a8" />


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

cut -c1-3 file1

cut -d "|" -f 1 file22

cut -d "|" -f 2 file22

## OUTPUT

<img width="553" height="372" alt="Screenshot (68)" src="https://github.com/user-attachments/assets/b9cb3936-fba6-4591-bf1f-db6e5a1de698" />

cat < newfile

```
Hello world
hello world
^d
```

cat > newfile

```
Hello world
hello world
```

<br>



<br>
grep Hello newfile


## OUTPUT

<img width="455" height="181" alt="Screenshot (69)" src="https://github.com/user-attachments/assets/0d89e58c-3204-45f5-a3a8-ed07bc23df33" />

## OUTPUT

grep -R ubuntu /etc

<img width="1927" height="994" alt="Screenshot (71)" src="https://github.com/user-attachments/assets/9bb25264-ab74-4ba5-a830-8b6aeb5276a6" />

## OUTPUT

grep -w -n world newfile
![s20](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/950eac77-02b0-47b7-b7e2-4ee02d0b4b16)


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
![s21](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/03363e61-7734-4512-a706-56d2100639cc)


<br>
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

egrep -w '(H|h)ello' newfile

<img width="589" height="413" alt="Screenshot (72)" src="https://github.com/user-attachments/assets/3124f6ea-1e37-4630-86c3-d32610fbccad" />


## OUTPUT



## OUTPUT

egrep '(World$)' newfile
<img width="684" height="258" alt="Screenshot (73)" src="https://github.com/user-attachments/assets/cf00aac5-208f-404e-8aa2-a74f4073e1a2" />

## OUTPUT

egrep 'Linux.\*world' newfile

## OUTPUT

egrep 'Linux.\*World' newfile

## OUTPUT

egrep l{2} newfile

<img width="610" height="107" alt="Screenshot (74)" src="https://github.com/user-attachments/assets/38f80b39-0a8c-45a4-91a3-4bdfc4d77f36" />


## OUTPUT

egrep 's{1,2}' newfile

![s32](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/59a2f0a4-15e0-4862-bafd-1c492bdfa5d9)
)

## OUTPUT

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

sed -e 's/Ram/Sita/' file23

<img width="564" height="480" alt="Screenshot (75)" src="https://github.com/user-attachments/assets/77fdbf00-a451-4107-b26e-889d33e67b15" />


## OUTPUT

sed -e '2s/Ram/Sita/' file23

sed '/tom/s/5000/6000/' file23

sed -n -e '1,5p' file23

sed -n -e '2,/Joe/p' file23


<img width="634" height="900" alt="Screenshot (76)" src="https://github.com/user-attachments/assets/49284bcc-1368-4d13-abef-aa1113c70fdf" />


## OUTPUT

sed -n -e '/tom/,/Joe/p' file23
seq 10

seq 10 | sed -n '4,6p'

seq 10 | sed -n '2,~4p'

seq 3 | sed '2a hello'

seq 2 | sed '2i hello'

seq 10 | sed '2,9c hello'

sed -n '2,4{s/^/$/;p}' file23

<img width="569" height="817" alt="Screenshot (77)" src="https://github.com/user-attachments/assets/04eea3ea-a163-43b2-9138-e15c0ea52260" />

## OUTPUT

sed -n '2,4{s/$/\*/;p}' file23
![s49](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/88ee8a96-e164-4878-b665-60f66793e1c4)


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

cat > file22

```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```
![s51](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/c2fec405-9b98-4e5d-a114-269892b859f0)

uniq file22
<img width="559" height="592" alt="Screenshot (78)" src="https://github.com/user-attachments/assets/e5db9fa4-0e94-4129-b7a1-cdb41dc119a2" />


## OUTPUT

# Using tr command

cat file23 | tr [:lower:] [:upper:]
![s53](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/e07b932d-209e-405a-bf03-0f32edcecab8)


## OUTPUT

cat < urllist.txt

```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
```
![s54](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/133d4864-e7c7-4bf7-a141-cc8fbd805709)


cat > urllist.txt

```
www. yahoo. com
www. google. com
www. mrcet.... com
```
![s55](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/71a56968-800f-463c-9799-9512a2f01504)


cat urllist.txt | tr -d ' '
![s56](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/668e6737-a302-4271-a827-0bb4bf53b973)


## OUTPUT

cat urllist.txt | tr -d ' ' | tr -s '.'
![s57](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/15ef2a8b-dce2-4a50-ac8e-46630a94b713)


## OUTPUT

# Backup commands

tar -cvf backup.tar \*
![s58](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/57874a59-a451-441a-a94b-72e84f9057a4)


## OUTPUT

mkdir backupdir

mv backup.tar backupdir
![s59](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/da330861-a256-4817-b254-49d0e8583dd0)


tar -tvf backup.tar
![s60](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/f8951454-beec-406a-a60e-06cc579604ce)


## OUTPUT

tar -xvf backup.tar
![s61](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/4d477976-0b07-4d9a-a733-8c2df2829ff7)


## OUTPUT

gzip backup.tar

ls .gz
![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/857d7982-00e5-4c2a-b9dd-2de602c1536d)

## OUTPUT

gunzip backup.tar.gz

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/37e7722a-af8b-4fac-9090-4a717a19263f)

## OUTPUT

# Shell Script

```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/97b7a17e-b989-4500-a84c-d43deea03ec0)

chmod 755 my-script.sh
./my-script.sh

![image](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/0fc185dd-d3be-4a80-8a20-605b7cbf426a)

## OUTPUT

cat << stop > herecheck.txt

```
hello in this world
i cant stop
for this non stop movement
stop
```
![s66](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/6798fbf7-79be-44b0-a85e-3ffb6386ad8d)


cat herecheck.txt
![s67](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/7fef5535-e5e5-43c1-aca7-e55bb3c24de9)


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
![s68](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/bed2223e-4039-437f-8022-c79fc9450dc9)



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
![s69](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/4b697cc1-bd43-4e44-9916-d6d6e7a8aa2e)


chmod 777 scriptest.sh

./scriptest.sh 1 2 3
![s70](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/fc64ec20-5d6c-42d9-aeac-a992c208e516)


## OUTPUT

ls file1
![s71](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/c558e2ec-c5d2-4663-8230-8151dd06a49b)


## OUTPUT

echo $?
![s72](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/f73a1a21-98b5-4886-9954-3d76b18a1d03)


## OUTPUT

./one
bash: ./one: Permission denied

echo $?
![s73](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/9f7a2aae-5224-4994-813c-205dc8ad6322)


## OUTPUT

abcd

echo $?
![s74](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/9596f3f7-ae59-4309-9c46-90f01dfe1a9f)


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
![s76](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/33da8183-c876-42ab-b0d0-5a6ef0c72fad)


## OUTPUT

chmod 755 strcomp.sh

./strcomp.sh
![s77](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/09ef6c4f-1aa1-4f49-804a-3cc43aa6ece0)


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
![s78](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/96143ae1-89d9-4ef1-83f9-968f96df60b7)


./psswdperm.sh
![s79](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/527fe054-e443-402b-8380-ffc9a0dcf36a)


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
![s81](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/d54c6b6b-ceb2-43f2-acf2-79be917cc115)



./ifnested.sh
![s80](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/474d1a23-d586-4808-9a67-001f6d78e252)


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
![s82](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/82668e74-1132-451a-8a36-32e4b0f2c688)


$ chmod 755 iftest.sh

$ ./iftest.sh

![s83](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/ebc6f63c-4f52-456a-90dd-faccc9615718)

## OUTPUT

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
![s84](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/4e1da425-fc48-447c-92f7-0f24fa98c76e)

$ chmod 755 ifnested.sh

$ ./ifnested.sh

![s85](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/b156efba-54d4-4aa6-8d13-346a5b34aba4)

## OUTPUT

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
![s86](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/fc9df084-2db1-4094-84af-4f34ba32eba7)


$ chmod 755 elifcheck.sh

$ ./elifcheck.sh
![s87](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/4ba8f3d9-32c0-4658-95eb-5bceb5771ed8)


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
![s88](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/67a3608e-c74c-4c46-8c2f-119e9a085fad)


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
![s89](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/80554d8c-d695-489c-8f2a-59d0c05159c6)


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
![s90](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/a1ca2d49-edca-4461-9f23-37a9becd2d64)


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
![s91](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/5187bbf5-2c8c-4427-9d88-76bbf12b8313)


cat forin1.sh

```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
![s92](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/623435f8-fdf2-4df3-a68c-fde3dc6a541b)


$ chmod 755 forin1.sh

$ ./forin1.sh
![s93](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/9661b3b2-3f46-450d-a8b3-b4275043c723)


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
![s94](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/f831e275-ef93-4bf4-9558-54d909c0ed92)


cat forin3.sh

```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ chmod 755 forin3.sh

$ ./forin3.sh
![s95](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/4ca8f75d-bf6a-4fa5-bc27-8bb34a90d688)



## OUTPUT

cat forinfile.sh

```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in "cat $file"
do
echo "Visit beautiful $state“
done
```

$ chmod 777 forinfile.sh

$ cat cities

Hyderabad <br>
Alampur      <br>
Basara<br>
Warangal<br>
Adilabad<br>
Bhadrachalam<br>
Khammam
<br>
![Screenshot 2024-03-08 114549](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/74770248-0e49-46ae-a44c-ebf12c5cc27c)


## OUTPUT

cat forctype.sh

```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
```

$ chmod 755 forctype.sh
$ ./forctype.sh
![s98](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/7887f468-52b2-402f-9c03-04066b841fc4)


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
![s99](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/2d6eb440-0b22-4f49-a854-1d94ef4dd77a)


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
![s100](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/b244e1df-a0e2-4e30-b5de-5722dd124373)


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
echo "The for loop is completed"
```

## OUTPUT

$ chmod 755 forbreak.sh

$ ./forbreak.sh
![s101](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/97e18019-46b5-4018-965d-e89ed48f6a1c)


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
echo "The for loop is completed"
```

$ chmod 755 forcontinue.sh

$ ./forcontinue.sh
![s102](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/a544cfc0-496e-4773-b21d-7da806471267)


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
![s103](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/c553768b-dfbf-4bad-8cc7-37874ba860ef)


## OUTPUT

cat exread1.sh

```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
```

$ chmod 755 exread1.sh

$ ./exread1.sh
![s104](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/cd6131ef-a7e8-492a-9659-7f74d1132b55)


## OUTPUT


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
![s105](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/6901226d-88c0-4f48-af4f-dcb87364be9f)


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
![s106](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/aa053f0c-670c-4837-859f-771ccfc31dcd)

cat argshift1.sh

```bash
args=("$@")
ELEMENTS=${#args[@]}
for (( i=0;i<$ELEMENTS;i++)); do
    echo ${args[${i}]}
done
```

$ chmod 777 argshift.sh

## OUTPUT

$ ./argshift.sh 1 2 3
![s107](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/12285fa6-26e7-4b6d-b64b-ba292200456f)


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
![s108](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/c7be0253-a039-46c7-b10a-76ae199141e5)


cat > nc.awk

```bash
BEGIN{}
{
print len=length($0),"\t",$0
wordcount+=NF
chrcnt+=len
}
END{}
{
print "total characters",chrcnt
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
```
![s109](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/e44165c1-43b1-4065-9409-2d66e20fc38a)


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
![s110](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/aaed686c-6e65-44f4-ba8f-068558bba2e8)


awk -f nc.awk data.dat

![s111](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/ca2d32f4-7cc3-49d4-bfa5-d976f219a692)



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

$ chmod 755 palindrome.sh

$ ./palindrome.sh

![s112](https://github.com/dharshan7200/OS-Linux-commands-Shell-script/assets/138850116/4eab42a8-e022-419a-8e59-f260a7b90c55)


# RESULT:

The Commands are executed successfully.
