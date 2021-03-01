# Assignment 2

## Copying specific files using `find`

1. Create three folders: /tmp/data/bolly, /tmp/data/holly and /tmp/datatolly [only 1 command]
    
    ```bash
    mkdir -p /tmp/data/bolly /tmp/data/holly /tmp/data/tolly
    ```
2.  Copy all the files in /etc starting with the letters a, b, c or d to tmp/data
    ```bash
    find /etc -name [a-d]* -type f -exec cp {} /tmp/data \;
    ```
3. Copy all the files in /etc starting with the letters a or b to /tmpdata/bolly
    ```bash
    find /etc -name [a-b]* -type f -exec cp {} /tmp/data/bolly \;
    ```
4. Copy all the files in /etc starting with the letters c or d to /tmpdata/holly
    ```bash
    find /etc -name [c-d]* -type f -exec cp {} /tmp/data/holly \;
    ```
5. Copy all the files in /etc that are larger than 40M to /tmp/data/tolly
    ```bash
    find /etc -size +40M -type f -exec cp {} tmp/data/tolly \;
    ```
6. Tar the three directories you have created and store the tar files in a folder on your desktop called MoviesData
    ```bash
    tar -cvf /home/bharatknv/Desktop/MoviesData/bolly.zip /tmp/data/bolly
    tar -cvf /home/bharatknv/Desktop/MoviesData/holly.zip /tmp/data/holly
    tar -cvf /home/bharatknv/Desktop/MoviesData/tolly.zip /tmp/data/tolly
    ```

