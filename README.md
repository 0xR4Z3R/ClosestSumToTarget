# ClosestSumToTarget

This is the simple java program to find closest sum to the target using Java progrom


import java.util.Arrays;

public class Target {
	
	public static void main(String[] args){
		
		//initilizing arrays
		
		int[] list1 = {12,32,14,8,12,9,20};
		int[] list2 = {8,-10,13,-29,1};
		
		//target
		int target = 24; 
		
		System.out.println("Array1:");
		
		System.out.println(Arrays.toString(list1));
		
		System.out.println("Array2:");
		
		System.out.println(Arrays.toString(list2));

		
		System.out.println("Find closest sum to the " + target);
		
    //call function
		closestToTarget(list1,list2,target);
		
	}
	
	public static void closestToTarget(int[] l1,int[] l2,int target) {
		
		
		int num1=0,num2=0;
		int x=target;
		
		
    
    // brute force attack :)))
    
		for(int e1: l1) {
			for(int e2: l2) {
				int sum = e1+e2;
				int y = Math.abs(sum-target);
				if(y<x){
					num1 = e1;
					num2 = e2;
					x=y;
					
				}
				
			}
		}
		
    //printing result
		System.out.println("["+ num1 + "," + num2 + "]");

		
		
	}
}
