#include <stdio.h>
int main(void) {
  int ROWS = 3, COLS = 3, i,j,sum=0;
  int num[3][3] = {
    {0,1,2},
    {4,5,6},
    {7,8,9}
  };
int *ptr = &num[0][0];
    for (i = 0; i < ROWS; i++) {
    for (j = 0; j < COLS; j++) {
      printf("%d ", *(ptr + i * COLS + j));
    }
    printf("\n");
  }
  for (i = 0; i < ROWS; i++) {
      sum = sum + *(ptr + i * COLS + i);
  }
  printf("Sum of diagonal is = %d ",sum);
}
