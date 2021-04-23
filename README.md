#include <stdio.h>

int main() 

{

char s[1000];
int i, v, c;

printf("Input sentence: ");
gets(s);

i=0;
while(s[i]!='\0')
    {
        if(s[i]=='a' ||s[i]=='e' ||s[i]=='i' ||s[i]=='o' ||s[i]=='u')
           s[i]=s[i]-32;
           i++;
     
    }
    
        v = 0, c = 0;
        for (int i = 0; s[i] != '\0'; ++i) {
        
        if (s[i] == 'a' || s[i] == 'e' || s[i] == 'i' ||
            s[i] == 'o' || s[i] == 'u' || s[i] == 'A' ||
            s[i] == 'E' || s[i] == 'I' || s[i] == 'O' ||
            s[i] == 'U') {
            ++v;
            
    }   else if ((s[i] >= 'a' && s[i] <= 'z') || (s[i] >= 'A' && s[i] <= 'Z')) { 
            ++c;
    }
    }
    
    printf("\nString Converted: ");
    puts(s);
     

printf("\nLength of String: %d\n", i);

printf("\nVowels: %d\n", v);

printf("\nConsonants: %d\n", c);

return 0;

}
