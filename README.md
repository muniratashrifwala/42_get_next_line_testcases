# get_next_line_42_testcases
This file contains different ways to test your Get_Next_Line project.

## For get_next_line ##

**Test Case 1 ->** <br>
(With text file)<br>
```
gcc get_next_line.c get_next_line_utils.c main.c
O/P -> (Print what is in the textfile)
```

**Test Case 2 ->**<br>
(Without text file)<br>
```
gcc get_next_line.c get_next_line_utils.c main.c 
O/P -> (Print nothing but it should not break / give error)
```

**Test Case 3 ->**<br>
(With buffer size as negative)<br>
```
gcc get_next_line.c get_next_line_utils.c main.c -D BUFFER_SIZE=-10
O/P -> (Print nothing but it should not break / give error)
```

**Test Case 4 ->**<br>
(With buffer size as 0) <br>
```
gcc get_next_line.c get_next_line_utils.c main.c -D BUFFER_SIZE=0
O/P -> (Print nothing but it should not break / give error)
```

**Test Case 5 ->** <br>
(With fd given as 0)<br>
```
gcc get_next_line.c get_next_line_utils.c main.c 
O/P -> (Print what is typed in the terminal)
```

**Test Case 6 ->** <br>
(With Buffer size as INT_MAX)<br>
```
gcc get_next_line.c get_next_line_utils.c main.c -D BUFFER_SIZE=2147483647
O/P -> (Is should allocate INT_MAX value without giving an error)
```

**Test Case 7 ->**<br>
(With Buffer size more than INT_MAX)<br>
```
gcc get_next_line.c get_next_line_utils.c main.c -D BUFFER_SIZE=2147483648
O/P -> (Is should return NULL and also not give any errors)
```

**Test Case 8 ->** <br>
(With a very big text file)<br>
```
gcc get_next_line.c get_next_line_utils.c main.c
O/P -> (Print what is in the big textfile)
```

**Test Case 9 ->** <br>
(Check for memory leaks with Valgrind)<br>
```
gcc get_next_line.c get_next_line_utils.c main.c
$ valgrind --leak-check=full ./a.out
```

**Test Case 10 ->** <br>
(With the Buffer size exactly as the size of the characters in the textfile)<br>
```
gcc get_next_line.c get_next_line_utils.c main.c -D BUFFER_SIZE=75 //example
O/P -> (Print what is in the textfile)
```


## For get_next_line_bonus ##

**Test Case 1 ->** <br>
(With 2 text files)<br>
```
gcc get_next_line_bonus.c get_next_line_utils_bonus.c main.c
O/P -> (Print what are in the textfiles)
```

**Test Case 2 ->** <br>
(With 1 text that exists and 1 that does not)<br>
```
gcc get_next_line_bonus.c get_next_line_utils_bonus.c main.c
O/P -> (Print what is in the textfile 1 and null for the non existing file)
```

**(Same as above test cases)**<br>
