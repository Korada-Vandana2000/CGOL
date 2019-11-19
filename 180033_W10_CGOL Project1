/*
 ============================================================================
 Name        : CGOL.c
 Author      : Korada Vandana
 Version     :
 Copyright   : Your copyright notice
 Description : Hello World in C, Ansi-style
 ============================================================================
 */
#include<stdio.h>
int main(){
    int const WIDTH = 5;
    int const HEIGHT = 5;
    int const CYCLES =3 ;
    int grid[HEIGHT][WIDTH];
    int temp[HEIGHT][WIDTH];

    int row;
    int col;
    for(row = 0; row < HEIGHT; row++){
        for(col = 0; col < WIDTH; col++){
            grid[row][col] = 0;
        }
    }
    int i;
    int x;
    int y;
    int neighbours;
    for(i = 0; i < CYCLES; i++){
        for(row = 0; row < HEIGHT; row++){
            for(col = 0; col < WIDTH; col++){
                temp[row][col] = 0;
            }
        }
        for(row = 0; row < HEIGHT; row++){
            for(col = 0; col < WIDTH; col++){
                neighbours = 0;
                for(y = -1; y < 2; y++){
                    for(x = -1; x < 2; x++){
                        if(x != 0 && y != 0 && grid[(row + y) % HEIGHT][(col + x) % WIDTH] == 1){
                            neighbours++;
                        }
                    }
                }
                if(grid[row][col] == 1){
                    if(neighbours < 2 || neighbours > 3){
                        temp[row][col] = 0;
                    }else{
                        temp[row][col] = 1;
                    }
                }else if(grid[row][col] == 0){
                    if(neighbours == 3){
                        temp[row][col] = 0;
                    }else{
                        temp[row][col] = 1;
                    }
                }
            }
        }
        for(row = 0; row < HEIGHT; row++){
            for(col = 0; col < WIDTH; col++){
                grid[row][col] = temp[row][col];
                printf("%d", grid[row][col]);
            }
            printf("\n");
        }
        printf("\n");
    }
}
