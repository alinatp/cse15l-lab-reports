# Lab Report 3 - Researching Commands

## Command : `find`

1.Command `-maxdepth`

Source: [Find Command -maxdepth](https://www.redhat.com/sysadmin/linux-find-command)

Input:
```
find ./technical -maxdepth 1
```

Output:
```
./technical
./technical/government
./technical/plos
./technical/biomed
./technical/911report
```

Input:
```
find ./technical -maxdepth 2
```

Output:
```
...
./technical/911report/chapter-1.txt
./technical/911report/chapter-5.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-9.txt
./technical/911report/chapter-8.txt
./technical/911report/preface.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-10.txt
./technical/911report/chapter-11.txt
```

What does it do?
* the `-maxdepth` command limits the depth of searches you do in the directory. In the first example the depth
 is 1 which is why only the names fo the files are show. In the second example the depth is 2 which shows
 all the text files.
 
 ---
 
 2. Command `-name`
 
 Source: [Find Command -name](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/)
 
 Input:
 ```
 find ./technical -name "*.txt"
 ```
 
 Output:
 ```
 ...
 ./technical/911report/chapter-2.txt
./technical/911report/chapter-1.txt
./technical/911report/chapter-5.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-9.txt
./technical/911report/chapter-8.txt
./technical/911report/preface.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-10.txt
./technical/911report/chapter-11.txt
 ```
 
 Input:
 ```
 find ./technical -name 911report
 ```
 
 Output:
 ```
 ./technical/911report
 ```
 
 What does it do?
 * The `-name` command searches the files that macthes the specific name.

---

3. Command `-empty`

Source: [Find Command -empty](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/)

Input:
```
find ./technical -empty
```

Output: With no empty text files
```

```

Input:
```
find ./technical -empty
```

Output: With an empty text file
```
./technical/911report/chapter-0.txt
```
 
 What does it do?
 * The `-empty` command finds any text file that is empty. In the first example there was no empty text file
   so nothing was found. In the second example there was 1 empty text file so it returned that file. 
   
---  
4. Command `-size`

Source: [Find command -size](https://linuxhandbook.com/find-command-examples/)

Input:
```
find ./technical -size 0k
```

Output:
```
./technical/911report/chapter-0.txt
```

Input:
```
find ./technical -size +150k -size -2G 
```

Output:
```
./technical/government/About_LSC/commission_report.txt
./technical/government/Env_Prot_Agen/multi102902.txt
./technical/government/Env_Prot_Agen/bill.txt
./technical/government/Env_Prot_Agen/tech_adden.txt
./technical/government/Gen_Account_Office/GovernmentAuditingStandards_yb2002ed.txt
./technical/government/Gen_Account_Office/Statements_Feb28-1997_volume.txt
./technical/government/Gen_Account_Office/pe1019.txt
./technical/government/Gen_Account_Office/d01591sp.txt
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-3.txt
```

What does it do?
* The `-size` command find files based on the size of the file. In the first example it's trying to find a
  a command that has the size of 0. In the second example is it finding files bigger than 150 KB but smaller
  than 2 GB.
