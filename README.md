Impledge Assessment

Overview:
Approach Dynamic Programming
Time Complexity: O(N^3)
Space Complexity: O(N)


The steps for execution of program

    1. I have taken inputs from the text file using cin.eof() and then saved it in query vector (it is end of file function which will return true if pointer reaches end of file)
    2. Then I made a function Allcompoundedwords() which will return me the vector of all strings made by compunding
    3. In Allcoumpoundedwords() I made a unordered_map<string,int> using query vector so that I can find strings easily, then I run a for loop from 0 to size of input array - 1 and cheacking each word
       if a word is made using compounding other words then return true otherwise return false this check is done by WB function.
    4. In WB() I have taken unordered_map of query vector and compounded string here I used Dynamic programming approach 
    5. In this I made a vector<bool> of size compounded word size +1 and initialised dp[0]=true then I used nested for loops in which outer one goes from 1 to dp.size() and inner one goes from 0 to i-1
    6. After that I have taken check substring from j to i
    7. then checking condition if dp[j] previous word was true and check is present in unordered_map of query and check is not wqual to compoundedword string then we will assign dp[i]=true
           condition : dp[j] && dict.find(check) != dict.end() && check != s
    8.otherwise we will return dp[i] = false
    9. after all execution of Allcompoundedwords() I got vector of all compounded words then I sort it according to size of each compounded string
    10. Using compare function which passed in sort function.
    11. then I printed last two elements of sorted vector.
    12. I used chrono.h file to find execution time in micro seconds then I multiplied it by 10^-3 and got precised value of milli seconds upto 6 precisions
    13 I printed the time taken then
