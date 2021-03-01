# Assignment 5

1. Write a bash script to print the multiplication table of a number provided by the user

    ```bash
    #! /bin/bash

    for i in {1..10}
    do
            echo "$1 * $i = $(($1 * $i))"
    done
    ```

2. Write a bash script to compare two strings and output whether or not they are the same

    ```bash
    #! /bin/bash

    echo -n "Enter a string: "
    read string1

    echo -n "Enter another string: "
    read string2

    if [ $string1 = $string2 ];
    then
            echo "Strings are the same"
    else
            echo "Strings are not the same"
    fi
    ```

3. Write a bash script to sort an array (Elements provided by the user)

    ```bash
    #! /bin/bash

    arr=( "$@" )

    for ((i = 0; i<$#; i++))
    do

        for((j = 0; j<5-i-1; j++))
        do

            if [ ${arr[j]} -gt ${arr[$((j+1))]} ]
            then
                # swap
                temp=${arr[j]}
                arr[$j]=${arr[$((j+1))]}
                arr[$((j+1))]=$temp
            fi
        done
    done

    echo ${arr[*]}
    ```

4. Write a bash script to search an array for an element (both provided by the user) and output the index of the element in the array

    ```bash
    #! /bin/bash

    arr=( "$@" )

    echo -n "Enter the element you want to search for: "
    read n

    for ((i = 0; i<$#; i++))
    do
        if [ $n == ${arr[i]} ]
        then
            echo "The element is present at $i"
            exit
        fi
    done

    echo "Element not present in array"
    ```
