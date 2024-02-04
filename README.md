#include <stdio.h>

int countSubstringOccurrences(char S1[], char S2[]) {

 int i, j, k, count = 0, M = strlen(S1), N = strlen(S2);

 for (i = 0; i <= N - M; i++) {

 for (j = 0; j < M; j++) {

 if (S2[i + j] != S1[j]) {

 break;

 }

 }

 if (j == M) {

 count++;

 }
}
return count;

}

int main() {

 char S1[100], S2[100];

 printf("Enter the first string S1: ");

 scanf("%s", S1);

 printf("Enter the second string S2: ");

 scanf("%s", S2);

 int occurrences = countSubstringOccurrences(S1, S2);

 printf("S1 appears as a substring in S2 %d times.\n", occurrences);

 return 0;

}
