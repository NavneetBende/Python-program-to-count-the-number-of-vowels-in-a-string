Count the number of vowels in a string
Program to Count the Number of vowels we’re going to check how many vowels are present in a given String . There are five vowels in English vocabulary, they are – ‘a’, ‘e’, ‘i’, ‘o’, ‘u’.

For Example, in the string prepinsta then in that case then vowesl are 3 (a,e,i)

Program count the number of vowels in a string
Algorithm
Step 1:- Start.
Step 2:- Take user input.
Step 3:- Initialize count variable.
Step 4:- Iterate through the string to find number of vowels.
Step 5:- Check if the alphabet of the string lies under the group of vowels.
Step 6:- If TRUE increment count by 1.
Step 7:- Print count.
Step 8:- End.
Python program to count number of vowels in a string
Run
#take user input
String = input('Enter the string :')
count = 0
#to check for less conditions
#keep string in lowercase
String = String.lower()
for i in String:
    if i == 'a' or i == 'e' or i == 'i' or i == 'o' or i == 'u':
        #if True
        count+=1
#check if any vowel found
if count == 0:
    print('No vowels found')
else:
    print('Total vowels are :' + str(count))
Output:
Enter the string :PrepInsta
Total vowels are :3
Note
The time complexity of above code in O(n) as in the code we are looping over the sting once
Method 2
Objective: Find number of vowels in string python

First take the string input in a string variable and make a function countVowels(str,str.length())
if the value of n that is (length of the string) is 1 then we will return. (This is the base case)
if the size of the string is not 1 then countVowels(str, n-1) + isVowel(str[n-1])
Here isVowel(str[n-1]) will be called if the character is vowel then this will return 1 otherwise 0
Program count the number of vowels
Objective: Given an alphabetical string ‘s’. count the number of vowels in it.

Run
# Function to check the Vowel
def isVowel(ch):
    return ch.upper() in ['A', 'E', 'I', 'O', 'U']

# to count total number of
# vowel from 0 to n
def countVovels(str, n):
    if (n == 1):
        return isVowel(str[n - 1]);
    return (countVovels(str, n - 1) +
                isVowel(str[n - 1]));
# Driver Code

# string object
str = "prepinsta";


# Total numbers of Vowel
print("Total numbers of Vowel =",countVovels(str, len(str)))
Total numbers of Vowel = 3
