# Assignment 3

1. Create 4 users with names tushar, nana, jaya and maulik
    
    ```bash
    # Run all the below commands as root

    useradd -m tushar

    useradd -m nana

    useradd -m jaya

    useradd -m maulik
    ```

2. Set expiry of password to 90 days

    ```bash
    # Run everything as root

    chage -M 90 tushar

    chage -M 90 nana

    chage -M 90 jaya

    chage -M 90 maulik
    ```

3.  Create group marketing and add tushar and nana to it

    ```bash
    # Run everything as root

    groupadd marketing

    gpasswd -M tushar,nana marketing
    ```
4. Create group it add jaya, maulik

    ```bash
    # Run everything as root

    groupadd it

    gpasswd -M jaya,maulik it
    ```

5. Create group as capgemini and add all users as secondary group to it

    ```bash
    # Run everything as root

    groupadd capgemini

    gpasswd -M tushar,nana,jaya,maulik capgemini
    ```

6. Try the input direction to set the password for all the users
    
    ```bash
    # Run everything as root

    passwd tushar
   
    passwd nana
   
    passwd jaya
   
    passwd maulik
    ```

7. Do the following in a single command
    1. Add a new user with the user id 2001. The name can be anything

    2. Set the shell for that user to {sh shell}

    3. Add this user into the existing group named Capgemini

    ```bash
    # Run everything as root

    useradd -m -u 2001 -s /bin/sh -G capgemini uiduser
    ```




