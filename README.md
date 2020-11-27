# MyGittub
A little things
import java.util.Scanner;

/**
 * @Author: Zhong Jing Quan
 * @Data: 2020/11/24-11-13:46
 * @Description: array
 * @Version: 12.0.1
 * 查找数组中某个元素，并返回下标
 */
public class ArrayTest02 {
    public static void main(String[] args) {
        int [] arr=new int []{-98,-22,0,4,23,26,64,100};
        Scanner  sc= new  Scanner (System.in);
        System.out.println("请输入要查找的数字：");

        int dest = sc.nextInt();
        int head=0,end= arr.length -1;
        boolean isFlag= false;
        while(head<=end ){
            int middle=(head+end)/2;
            if (dest==arr[middle]){
                System.out.println("找到了指定的元素，位置为"+middle);
                isFlag=true;
                break;
            }
            else if(arr[middle]>dest){
             end=middle-1;
            }
            else  /* arr[middle]<dest*/ {
                head =middle+1;
            }
        }
        if(!isFlag){
            System.out.println("很遗憾，没有找到！");
        }
    }
}
