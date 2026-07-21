# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER
Name ; TINU MATHEW M
## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main() {
    char text[100];
    int key, i;

    printf("Enter the text: ");
    fgets(text, sizeof(text), stdin);

    printf("Enter the key: ");
    scanf("%d", &key);

    
    for (i = 0; text[i] != '\0'; i++) {
        if (text[i] >= 'A' && text[i] <= 'Z')
            text[i] = ((text[i] - 'A' + key) % 26) + 'A';
        else if (text[i] >= 'a' && text[i] <= 'z')
            text[i] = ((text[i] - 'a' + key) % 26) + 'a';
    }

    printf("Encrypted Text: %s", text);

   
    for (i = 0; text[i] != '\0'; i++) {
        if (text[i] >= 'A' && text[i] <= 'Z')
            text[i] = ((text[i] - 'A' - key + 26) % 26) + 'A';
        else if (text[i] >= 'a' && text[i] <= 'z')
            text[i] = ((text[i] - 'a' - key + 26) % 26) + 'a';
    }

    printf("Decrypted Text: %s", text);

    return 0;
}
```

## OUTPUT:

<img width="1600" height="900" alt="WhatsApp Image 2026-07-21 at 14 47 39" src="https://github.com/user-attachments/assets/222fffe0-7d52-42ef-ad0c-ce7242c61d98" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
