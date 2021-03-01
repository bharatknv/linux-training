# Assignment 4

1.  Set the umask value to 002 permanently

    ```bash
    echo "umask 002" | tee -a /home/$USER/.bashrc
    ```

2. Again change the umask value to the default value

    ```bash
    echo "umask 022" | tee -a /home/$USER/.bashrc
    ```

3. You need create files by root & see that other user & group can't access them

    ```bash
    chmod 700 # Run as root
    ```

4. Files created by other user can be accessed by the group owners
    ```bash
    chmod 660
    ```

5. Create a directory on the desktop with the name as CapgeminiFolder

    ```bash
    mkdir ~/Desktop/CapgeminiFolder
    ```

    1. Make sure the members of the group i.e "bigdata" should be able to
access the data inside the directory

        ```bash
        chown -R :bigdata ~/Desktop/CapgeminiFolder
        ```
    
    2. and that other users can't access it

        ```bash
        chmod 770 ~/Desktop/CapgeminiFolder
        ```
    
    3. Make sure one thing one user can't access or write the file of other user
present in the above shared directory

        ```bash
        chmod 660 ~/Desktop/CapgeminiFolder/*
        ```


