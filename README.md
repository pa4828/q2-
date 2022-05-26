# q2-
Given a sentence,s, print each word of the sentence in a new line. 
Input Format 
The first and only line contains a sentence, .
Constraints   
1<=len(s)<=1000
Output Format 
Print each word of the sentence in a new line.  
Sample Input 0 
This is C  
Sample Output 0  
This is C
Explanation 0 
In the given string, there are three words ["This", "is", "C"]. We have to print each of these words in a new line.
Sample Input 1 
Learning C is fun 
Sample Output 1 
Learning 
C
is
fun
Sample Input 2  
How is that
Sample Output 2 
How
is
that

#include <stdio.h>
#include <stdlib.h>
#include <math.h>
#include <string.h>

int main()
{
    char *s;
    s = malloc(1024 * sizeof(char));
    scanf("%[^\n]", s);
    s = realloc(s, strlen(s) + 1);
    int len = strlen(s);
    for(int i = 0; i < len; i++) {
        if(s[i] == ' ') {
            printf("\n");
        }
        else {
            printf("%c", s[i]);
        }
    }
    free(s);
    return 0;
}
