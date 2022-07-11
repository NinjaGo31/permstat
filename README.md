# How to Use permstat.c
permstat.c takes an existing regular file, reads the permissions of the file in octal format, and returns the permission string in character form.

## Arguments
Only one file can be provided as an argument. If there is not exactly two argument, a usage statement will be printed.
![image](https://user-images.githubusercontent.com/56609280/178348106-60a04b26-9388-4657-831b-c784aa81858b.png)

## Functions
permstat uses the stat command to obtain information about that file. If stat returns a value less than 0, an error will be printed out.
![image](https://user-images.githubusercontent.com/56609280/178348228-c6a447de-048e-4d66-9a3b-fb0445d4a7ef.png)

After obtaining the file's information, it check if the file is a regular file. Otherwise, an error will be printed.
![image](https://user-images.githubusercontent.com/56609280/178351581-0848ece5-5016-47fc-8f64-016f53de4ace.png)

The permission_string function takes the permission strings in octal form and uses permission macros (e.g.: S_IRUSR = User read permission macro). If the file has that permission, either a 'r','w', or 'x' will be added to the string. Otherwise, there will be a '-', meaning the file does not grant a certain permission for either the user, group, or other. Afterwards, the permission string will be printed.
![image](https://user-images.githubusercontent.com/56609280/178351682-2138a52e-37f7-45fa-a29d-3994b99e4e90.png)
