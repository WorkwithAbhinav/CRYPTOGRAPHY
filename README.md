# CRYPTOGRAPHY
Code to encrypt and decrypt a messages 










#include<stdio.h>
#include<string.h>
char string[1000];
char cipher[100][100];
int i,j,k=0;
int row;
int nrows()
{
int length;
length = strlen(string);
if(length % 3 == 0) 
row = length / 3 ;
else
row = (length / 3) + 1;
}
void encrypt()
{
 printf("\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\n");
 printf("The Encrypted Message is: \t");
 
row = nrows();
for(i = 0; i < row; i++)
{
for(j = 0; j < 3; j++)
{
if(string[k] != '\0')
cipher[i][j] = string[k++];
else 
cipher[i][j] = '*';
}
}
for(j = 0; j < 3; j++)
for(i = 0; i < row; i++){
printf("%c",cipher[i][j]);}
 printf("\n\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\n");
}
void decrypt()
{
 printf("\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\n");
 printf("The Decrypted Message is: \t");
 
row = nrows();
for(j = 0; j < 3; j++)
for(i = 0; i < row; i++)
cipher[i][j] = string[k++];
for(i = 0; i < row; i++)
{
for(j = 0; j < 3; j++)
{
if(cipher[i][j] != '*'){
printf("%c",cipher[i][j]);}
}
}
 printf("\n\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\n");
}
int main()
{
int option;
printf("-------------------------------------------------------------------\n");
printf("Enter the Message\n");
gets(string);
printf("\n\n");
printf("\nWhat do you want to do? \n1: Encrypt the Message 2: Decrypt the Message\n\n"); 
scanf("%d",&option);
if(option == 1)
encrypt();
else
decrypt();
 printf("-------------------------------------------------------------------\n");
 
 printf("\n\n\n");
return 0;
}







[cryptography.pdf](https://github.com/WorkwithAbhinav/CRYPTOGRAPHY/files/10022778/cryptography.pdf)

