TASK 13 

cd holbertonschool-shell/io_redirections_and_filters
touch 13-unique
chmod +x 13-unique

#!/usr/bin/env bash
sort | uniq -c | awk '$1 == 1 {print $2}' | sort

cat > list << EOF
C#
C
Javascript
Perl
PHP
PHP
ASP
R
Go
C#
C++
R
Perl
Javascript
Javascript
Python
Javascript
Javascript
Javascript
Java
Java
Python
Javascript
Javascript
Javascript
ASP
EOF

cat list | ./13-unique
git add io_redirections_and_filters/13-unique
git commit -m "Add script to print unique words sorted alphabetically"
git push origin main


Task 14 

cd ~/holbertonschool-shell/io_redirections_and_filters

echo 'grep root /etc/passwd' > 14-findthatword
chmod +x 14-findthatword

./14-findthatword

git add io_redirections_and_filters/14-findthatword
git commit -m "Add script to display lines containing 'root' from /etc/passwd"

Task 15
echo 'grep -c bin /etc/passwd' > 15-countthatword
chmod +x 15-countthatword

./15-countthatword
You should see a number like: 81


git add io_redirections_and_filters/15-countthatword
git commit -m "Add script to count lines containing 'bin' in /etc/passwd"

Task 16
echo 'grep -A 3 root /etc/passwd' > 16-whatsnext
chmod +x 16-whatsnext

./16-whatsnext
You should see blocks of lines with "root" followed by the next 3 lines, separated by --.
git add io_redirections_and_filters/16-whatsnext
git commit -m "Add script to display lines with 'root' and 3 following lines from /etc/passwd"

task 17
echo 'grep -v bin /etc/passwd' > 17-hidethisword
chmod +x 17-hidethisword

./17-hidethisword
You should see lines from /etc/passwd that do not include the word bin

git add io_redirections_and_filters/17-hidethisword
git commit -m "Add script to display lines that do not contain 'bin' from /etc/passwd"

Task 18
echo "grep '^[a-zA-Z]' /etc/ssh/sshd_config" > 18-letteronly
chmod +x 18-letteronly

./18-letteronly
 It should show only lines that begin with a letter (ignoring comments, empty lines, etc.).

git add io_redirections_and_filters/18-letteronly
git commit -m "Add script to show lines starting with letters from sshd_config"

Task 19
echo "tr 'Ac' 'Ze'" > 19-AZ
chmod +x 19-AZ

echo 'Replace all characters `A` and `c` from input to `Z` and `e`.' | ./19-AZ
Output should be:
Replaee all eharaeters `Z` and `e` from input to `Z` and `e`.

git add io_redirections_and_filters/19-AZ
git commit -m "Add script to replace A with Z and c with e from input"

Task 20

echo "tr -d 'cC'" > 20-hiago
chmod +x 20-hiago

echo Chicago | ./20-hiago

Output:hiago

git add io_redirections_and_filters/20-hiago
git commit -m "Add script to remove characters c and C from input"

Task 21

echo "rev" > 21-reverse
chmod +x 21-reverse

echo "Reverse" | ./21-reverse
Expected output:esreveR

git add io_redirections_and_filters/21-reverse
git commit -m "Add script to reverse input using rev"

Task22

#!/bin/bash
cut -d: -f1,6 /etc/passwd | sort

chmod +x 22-users_and_homes
./22-users_and_homes

git add io_redirections_and_filters/22-users_and_homes
git commit -m "Add script to list users and home directories sorted by user"





