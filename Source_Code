import java.util.Scanner;
public class th5 {
    public static void main(String[]args){
        Scanner sc=new Scanner(System.in);
        int[][]arr2d={
                {0, 0, 10, 0, -1},
                {0, -1, 0, 0, -1},
                {-1, 0, -1, 0, 0},
                {0, -1, 7, 0, -1},
                {0, -1, 0, -1, 0}
        };
        System.out.println("Initial Map: ");
        printmap(arr2d);
        int row= arr2d.length;
        int col=arr2d[0].length;
        int row_pos=-1, col_pos=-1;
        for(int i=0;i<row;i++){
            for (int j=0;j<col;j++){
                if(arr2d[i][j]==7){
                    row_pos=i;
                    col_pos=j;
                    break;
                }
            }
        }
        int turns=5;
        while(turns>0){
            System.out.println("Enter your move: "+(6-turns));
            String inp=sc.nextLine();
            int new_row=row_pos;
            int new_col=col_pos;
            switch (inp){
                case"Up":new_row--;break;
                case "Down":new_row++;break;
                case"Left":new_col--;break;
                case "Right":new_col++;break;
                default:
                    System.out.println("Invalid move!");
                    continue;
            }
            if(new_row<0||new_row>=row||new_col<0||new_col>=col){
                System.out.println("You moved outside the grid. GAME OVER for you Bitch!");
                return;
            }
            if(arr2d[new_row][new_col]==-1){
                System.out.println("BOOM! Stepped on a Mine. You deserved that :) !!");
                return;
            } else if (arr2d[new_row][new_col]==10) {
                arr2d[row_pos][col_pos]=0;
                arr2d[new_row][new_col]=7;
                System.out.println("Congrats!! King! Go live with your luxury.");
                System.out.println("Final State: ");
                printmap(arr2d);
                return;
            }
            arr2d[row_pos][col_pos]=0;
            arr2d[new_row][new_col]=7;
            row_pos=new_row;
            col_pos=new_col;
            System.out.println("Current State: ");
            printmap(arr2d);
            turns--;
        }
        System.out.println("You pathetic loser!");
    }


    public static void printmap(int[][]arr){
    for(int i=0;i< arr.length;i++){
        for(int j=0;j< arr[0].length;j++){
            System.out.print(arr[i][j]+" ");
            }
        System.out.println();
        }    
    }
}
    
