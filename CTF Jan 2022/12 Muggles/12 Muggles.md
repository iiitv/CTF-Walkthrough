
# Welcome to Hogwarts


## Link to the Question

[Click here](https://find-the-evil.netlify.app/)

## Answer

```
flag{YEAHITSMEWORMTAIL}

```

## Solution


As the Question clearly states the word "genes", it is a clear indication of DNA Cipher. Second hint for the same was in the Code where the terms AGCT are used which are the 4 types of DNA molecules present namely adenine (A), cytosine (C), guanine (G), and thymine (T).

## Answer

```

TAGCTGCGGGACGAGGTCGTAGCGCTGTAAGGAGGTGCGGTCCGGGAGGCC

```

Though to decrypt the cipher you will need to download the image of wormtail.(the name of the file is huehuehuehint.jpeg)
![Hint](./huehuehuehint.jpeg)

The cipher code is hidden in the image using steganography, so to run the file you will need a password! The password is this is "genes". After decrypting this it will take you to a google drive which contains the dna_code.

![Debugging](./Debugging.PNG)

This response clearly suggests that when you enter some username and password this is the query which is running on the backend database. But the username and password are not being used as is inside the query. After trying multiple times for multiple combinations of username and password or simply entering all the alphabets inside the username and password fields you can easily crack the cipher. The cipher is actually shift cipher

For username the characters are shifting 4 characters ahead and for the password the characters are getting shifted 17 characters ahead. So to have any query which we want to run we'll have to enter some string in username which will be 4 characters behind and and a string in password which will be 17 characters behind.

Now we need to enter admin as username and anything in password to carry out sql injection.
Note. You'll have to put 0 in the debugging cookie to actually log in. 
For example if you want to execute the following query:
```
SELECT * from Users where username = 'admin' and password = '' or 1=1 #
```
You will have to enter ```wziej``` in the username and ```' XA 1=1 #``` in password.

After this you will have successfully logged in.

On the next page you'll have input field to enter any sql query you want on the database.

To go ahead first you need to enter the following two queries.

```Show tables```
This will show all the tables in the database which are user table and information table.
```Select * from Information```
This will give you a drive link which will be a chrome extension.
You need to unpack the chrome extension and look into the manifest.json file to find the that the extension only works on the following website:
``` https://unsplash.com/s/photos/web ```
After this you have to load the extension in the browser and visit the above website.
![Debugging](./Flags.PNG)
On this website you need to click on one of the small flags to open a image which will contain half the flag.
Then you have to go back to the original website and upload this image along with the first half of the flag to get the complete flag. 
