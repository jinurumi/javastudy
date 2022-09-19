# javastudy


package src.jinhye;

/**
 * 8월 29일(월) 부터 9월 3일 (토)
 *
 * 두명의 플레이어가 있고 무한 반복문으로 게임 시작을 물어봅니다.
 * 예스 라면 한명이 주사위를 던집니다.
 * 또 다른 한명이 주사위를 던집니다.
 * 더 큰 수가 나온 사람이 승리 입니다.
 *
 * 노 라면 게임을 종료합니다.
 ***
 */

import java.util.*;

public class DiceGame {
    public static void main(String[] args) {

        int player1;
        int player2;
        Scanner sc = new Scanner(System.in);

        int[] dice = {1,2,3,4,5,6};


        while(true){
            System.out.println("게임을 시작하시겠습니까?(yes or no)");
            String ans;
            ans = sc.nextLine();

            if(ans.equals("yes")){
                double random=Math.random();
                int num = (int)Math.round(random* (dice.length-1));

                player1=dice[num];
                System.out.println("player1은 "+player1+"가 나왔습니다.");

                player2=dice[num];
                System.out.println("player2은 "+player2+"가 나왔습니다.");

                if(player1>player2){
                    System.out.println("player1이 이겼습니다.");



                }
                else if(player1<player2){
                    System.out.println("player2이 이겼습니다.");
                }
                else {
                    System.out.println("비겼습니다.");
                }


            }
            else {
                break;
            }


        }







    }
}

