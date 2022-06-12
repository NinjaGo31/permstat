# How to Use permstat.c
permstat.c takes an existing regular file, reads the permissions of the file in octal format, and returns the permission string in character form.

## Arguments
Only one file can be provided as an argument. If there is not exactly two argument, a usage statement will be printed.
![image](https://user-images.githubusercontent.com/56609280/173249565-63dd0d25-6635-4cc6-817c-b29f37d6eb3f.png)

## Functions
permstat uses the stat command to obtain information about that file. If stat returns a value less than 0, an error will be printed out.
![image](https://user-images.githubusercontent.com/56609280/173249592-54a3c4ab-90ec-4f70-994b-694ea80e7950.png)

After obtaining the file's information, it check if the file is a regular file. Otherwise, an error will be printed.
![image](https://user-images.githubusercontent.com/56609280/173249607-cfdfa558-4431-4cb8-9134-49a24b40c7e0.png)

The permission_string function takes the permission strings in octal form and uses permission macros (e.g.: S_IRUSR = User read permission macro). If the file has that permission, either a 'r','w', or 'x' will be added to the string. Otherwise, there will be a '-', meaning the file does not grant a certain permission for either the user, group, or other. Afterwards, the permission string will be printed.
![image](https://user-images.githubusercontent.com/56609280/173249617-900d5fed-1b21-4b7d-8f9d-a56205888c3c.png)
