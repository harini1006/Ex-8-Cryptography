# Ex-8-Implement-the-AES-Encryption-and-Decryption
## AIM :
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

## ALGORITHM :
Step 1: AES is based on a design principle known as a substitution–permutation.

Step 2: AES does not use a Feistel network like DES, it uses variant of Rijndael.

Step 3: It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.

Step 4: AES operates on a 4 × 4 column-major order array of bytes, termed the state.

## PROGRAM :
```
Developed by:Harini V
Register no: 212222230044
```
```c
#include <stdio.h>
#include <string.h>

void xor_encrypt_decrypt(char *input, char *key) {
    int input_len = strlen(input);
    int key_len = strlen(key);

    for (int i = 0; i < input_len; i++) {
        input[i] = input[i] ^ key[i % key_len]; 
    }
}

int main() {
    char url[256], key[256];

    // Asking for user input
    printf("Enter the URL/string to encrypt: ");
    fgets(url, sizeof(url), stdin);
    url[strcspn(url, "\n")] = '\0'; // Remove trailing newline from fgets

    printf("Enter the key for encryption: ");
    fgets(key, sizeof(key), stdin);
    key[strcspn(key, "\n")] = '\0'; // Remove trailing newline from fgets

    printf("Original URL: %s\n", url);

    xor_encrypt_decrypt(url, key);
    printf("Encrypted URL: %s\n", url);

    xor_encrypt_decrypt(url, key);
    printf("Decrypted URL: %s\n", url);

    return 0;
}
```
## OUTPUT:
![{7E194EAD-5155-4BBD-BCDE-B9909C7EA89C}](https://github.com/user-attachments/assets/8730f770-717c-43e0-a797-2af0f22451b1)

## RESULT:
Hence,to use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption is done successfully.
