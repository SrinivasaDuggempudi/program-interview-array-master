# Java Arrays Interview Questions and Answers

>Author : Srinivasa Duggempudi


### Table of Contents

| No. | Questions |
|---- | ---------
|1 | [Find a missing number?](#find-a-missing-number)|
|2 | [Find a multile duplicate numbers in the array?](#find-a-multile-duplicate-numbers-in-the-array)|
|3 | [Pair of numbers equal to sum?](#Pair-of-numbers-equal-to-sum)| 
|4 | [Number not present in second array ?](#Number-not-present-in-second-array)|
|5 | [Find a duplicate number in array?](#Find-a-duplicate-number-in-array)|
|6 | [Largest and smallest numbers of array?](#Largest-and-smallest-numbers-of-array)|
|7 | [Find second largest number in array?](#Find-second-largest-number-in-array)|
|8 | [Find top two maximum numbers?](#Find-top-two-maximum-numbers)|
|9 | [Reverse the array?](#Reverse-the-array)|
|10| [Reverse array without new array?](#Reverse-array-without-new-array)|
|11| [Insert element at end of the array?](#Insert-element-at-end-of-the-array)|
|12| [Insert an element at given Location?](#Insert-an-element-at-given-location)|
|13| [Delete element at end of the array?](#Delete-element-at-end-of-the-array)|
|14| [Delete the given element from array?](#Delete-the-given-element-from-array)|
|15| [What is a module?](#what-is-a-module)|
|16| [What is a module?](#what-is-a-module)|
|17| [What is a module?](#what-is-a-module)|
|18| [What is a module?](#what-is-a-module)|
|19| [What is a module?](#what-is-a-module)|
|20| [What is a module?](#what-is-a-module)|
|21| [What is a module?](#what-is-a-module)|
|22| [What is a module?](#what-is-a-module)|



|279| [](#)

1. ### Find a missing number?

Write a program in Java for, In array 1-100 numbers are stored, one number is missing how do you find it?
   ```
   package arrays;

public class A01_FindMissingNumber {

	// Function to find the missing number
	//{ 1, 3, 7, 5, 6, 2 };
    public static void findMissing(int arr[], int N)
    {
        int i;
        int temp[] = new int[N + 1];
        for (i = 0; i <= N; i++) {
            temp[i] = 0;
        }
  
        for (i = 0; i < N; i++) {
            temp[arr[i] - 1] = 1;
        }
        int ans = 0;
        for (i = 0; i <= N; i++) {
            if (temp[i] == 0)
                ans = i + 1;
        }
        System.out.println(ans);
    }
    // Driver Code
    public static void main(String[] args)
    {
        int arr[] = { 1, 3, 7, 5, 6, 2 };
        int n = arr.length;
  
        // Function call
        findMissing(arr, n);
    }
}
   
 ```
   Output :
   
  ```
     4
  ```

  **[⬆ Back to Top](#table-of-contents)**

2. ### Find a multile duplicate numbers in the array?
    
    Write a program in Java for, In a array 1-100 multiple numbers are duplicates, how do you find it.
    
    ```
     package arrays;

         public class A02_MultipleNumbersDuplicate {

	//2.	Write a program in Java for, In a array 1-100 multiple numbers are duplicates, how do you find it.
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		int arr [] = {2,3,2,5,6,5,7,1,4,8,4,7,1};
		
		for(int i=0 ; i< arr.length ; i++) {
			int count =0;
			for(int j=i ; j < arr.length ; j++) {
				
				if(arr[i] == arr[j]) {
				count = count+1;
				}
				
				if(count == 2) {
					System.out.print(" "+arr[j]);
					break;
				}
			}
		}
	   }
        }

     ```
      **Output :** 2 5 7 1 4
       

 **[⬆ Back to Top](#table-of-contents)**

3. ### Pair of numbers equal to sum?
  
   Write a program in Java for, How to find all pairs in array of integers whose sum is equal to given number.
   ```
      package arrays;
       public class A03_PairsOfIntegersEqualToSum {
	//3.	Write a program in Java for, How to find all pairs in array of integers whose sum is equal to given number.
	public static void main(String[] args) {
		
		int sum= 10;
		int arr[] = {1,2,3,4,5,6,7,8,9};
		
		for(int i=0 ; i< arr.length-1 ; i++) {
			
			for (int j=i+1 ; j < arr.length ;j++) {
				
				if(arr[i] + arr[j] == 10) {
					System.out.print("["+arr[i] + "," + arr[j]+"]"+",");
				}
			}
		}
	     }
      }   
   ```
   **output:**  [1,9],[2,8],[3,7],[4,6],
   

  **[⬆ Back to Top](#table-of-contents)**

4. ### Number not present in second array
     Write a program in Java for, Given two arrays 1,2,3,4,5 and 2,3,1,0,5 find which number is not present in the second array.
     ```
	                  package arrays;
         public class A05_NumberNotPresentInSecondArray {

	//5.	Write a program in Java for, Given two arrays 1,2,3,4,5 and 2,3,1,0,5 find which number is not present in the second array.
	public static void main(String[] args) {
		int arr1[] = {1,2,3,4,5};
		int arr2[] = {2,3,1,0,5};
		
		for(int i=0 ; i<arr1.length ; i++) {
			boolean ispresent = false;
			for(int j=0 ; j< arr2.length ; j++) {
				
				if(arr1[i] == arr2[j]) {
					ispresent= true;
				}
			}
			if(!ispresent) {
				System.out.println(arr1[i]);
			}
		    }
	         }
            }	
     ```
     **output :** 4
   
  **[⬆ Back to Top](#table-of-contents)**

5. ### Find a duplicate number in array??
     Write a program in Java for, Given two arrays 1,2,3,4,5 and 2,3,1,0,5 find which number is not present in the second array.
     ```
                  public class A04_FindDuplicate {

	   //5.	Write a program in Java for, Given two arrays 1,2,3,4,5 and 2,3,1,0,5 find which number is not present in the second array.
	      public static void main(String[] args) {
		
		int arr[] = {1,2,5,4,3,2,9};
		
		for(int i=0 ; i< arr.length-1 ; i++) {
			
			int count =1;
			for (int j= i+1; j<arr.length ; j++) {
				
				if(arr[i] == arr[j]) {
					count ++;
					if(count ==2){
						System.out.println(arr[i]);
					}
				   }
			       }
		           }
	                }
                      }
		      
     ```
   **output :** 2

  **[⬆ Back to Top](#table-of-contents)**

6. ### Largest and smallest numbers of array?
    Write a program in Java to find largest and smallest number in array
     ```
          public class A06_LargestAndSmallestNumber {
    //6.	Write a program in Java to find largest and smallest number in array
	public static void main(String[] args) {
		int arr[] = {1,2,3,4,5,6,7};
		
		int smallest = arr[0];
		int largest = arr[0];
		
		for(int i=1 ; i< arr.length; i++ ) {
			if(arr[i] < smallest) {
				smallest = arr[i];
			}
			
			if(arr[i] > largest) {
				largest = arr[i];
			}
		}
		System.out.println("Smallets:" + smallest + "   largest : "+largest);
	     }
         }     
     ```
     **OutPut:**  Smallets:1   largest : 7
  
  **[⬆ Back to Top](#table-of-contents)**

7. ### Find second largest number in array?
    Write a program in Java to find second highest number in an integer array.
    ```
        public class A07_SecondLargestNumberInArray {

	//7.	Write a program in Java to find second highest number in an integer array.
	public static void main(String[] args) {

      int []arr = {5,8,3,9,2,6};
      int largest =0;
      int secondLargest=0;
      
      for(int i=0 ; i< arr.length ; i++) {
    	  if(arr[i] > largest) {
    		  secondLargest = largest;
    		  largest = arr[i]; 
    	  }
      }
      System.out.println("Second Largest : " + secondLargest);
	}
      }
    ```
    **Output :**   Second Largest : 8
    
  **[⬆ Back to Top](#table-of-contents)**

8. ### Find top two maximum numbers?
```
    public class A08_TopTwoMaximumNumbers {

	//8.	Write a program in Java to find top two maximum number in array?
	
	public static void main(String[] args) {
		
		int arr[] = {9,7,2,5,4,11};
		int largest =0;
		int secondLargest =0;
		
		for(int i=0; i< arr.length ; i++) {
			
			if(arr[i] > largest) {
				secondLargest = largest;
				largest =arr[i];
			}
		}
		System.out.println("Largest : " +largest + " secondLargest :" + secondLargest);
	        }
           }

```
**Output :**  Largest : 11 secondLargest :9

  **[⬆ Back to Top](#table-of-contents)**

9. ### Reverse the array?

```
    public class A09_ReverseOrder {
	//9.	Java program to print array in reverse Order.
	public static void main(String[] args) {
		
		int arr[] = {9,8,7,6,5};
		int result[] = new int[arr.length];
		int index =0;
		
		for(int i=arr.length-1 ; i>=0 ; i--) {
			result[index] = arr[i];
			index++;
		}
		System.out.println(Arrays.toString(result));
	}
       }
```
**OutPut :** [5, 6, 7, 8, 9]

  **[⬆ Back to Top](#table-of-contents)**

10. ### Reverse array without new array?
```
           package arrays;
       import java.util.Arrays;
     public class A10_ReverseArrayWithoutSecondArray {
	
	//10. Java program to reverse the array without new array.
	public static void main(String[] args) {
			int arr[] = {9,8,7,6,5};
			
			int middle = arr.length/2;
			int j = arr.length-1;
			int temp =0;
			
		for(int i=0 ; i< middle ; i++ , j--) {
			
			temp =arr[i];
			arr[i]= arr[j];
			arr[j] = temp;
		}
		System.out.println(Arrays.toString(arr));
	}
    }
```
**OutPut :** [5, 6, 7, 8, 9]

  **[⬆ Back to Top](#table-of-contents)**
  
11. ### Insert element at end of the array??
```

package arrays;

    import java.util.Arrays;
    public class A11_InsertAtEndOfTheArray {

	//17.	Java Program to print all even numbers in array.
	public static void main(String[] args) {
		int givenNumber =10;
		int arr[] = {9,8,7,6,5};
		int newArr[] = new int[arr.length+1];
		
		for(int i=0 ; i< arr.length ; i++) {
			newArr[i] = arr[i];
		}
		
		newArr[arr.length] = givenNumber;
		System.out.println(Arrays.toString(newArr));
	 }
      }
```
**OUTPUT :** [9, 8, 7, 6, 5, 10]

  **[⬆ Back to Top](#table-of-contents)**
  
 12. ### Insert an element at given Location?
```
        package arrays;

    import java.util.Arrays;
    public class A12_InsertAtgivenLocation {

	// 12. Java program to insert an element at given Location
	public static void main(String[] args) {

		int[] arr = { 25, 14, 56, 15, 36, 56, 77, 18, 29, 49 };

		int givenIndex = 2;
		int newValue = 5;
		System.out.println("Original Array : " + Arrays.toString(arr));

		for (int i = arr.length - 1; i > givenIndex; i--) {
			arr[i] = arr[i - 1];
		}
		arr[givenIndex] = newValue;
		System.out.println("New Array: " + Arrays.toString(arr));
	}
     }
```
**OUTPUT :** 

Original Array : [25, 14, 56, 15, 36, 56, 77, 18, 29, 49]
New Array: [25, 14, 5, 56, 15, 36, 56, 77, 18, 29]

  **[⬆ Back to Top](#table-of-contents)**
  
 13. ### Delete element at end of the array?
```
            public class A13_DeleteAtEndOfArray {
	//11.	Java program to Delete element at end of the array?
	public static void main(String[] args) {
		int[] arr = { 25, 14, 56, 15, 36, 56, 77, 18, 29, 49 };
		
		int newArr[] = new int[arr.length-1];
		
		for(int i=0 ; i< arr.length ; i++) {
			
			if(i == arr.length-1) {
				continue ;
			}
			newArr[i] = arr[i];
		}
		System.out.println(Arrays.toString(newArr));
	}
     }    
```
**OUTPUT :**  [25, 14, 56, 15, 36, 56, 77, 18, 29]

  **[⬆ Back to Top](#table-of-contents)**
  
  14. ### Delete the given element from array?
```
    package arrays;

    import java.util.Arrays;
    public class A14_DeleteGivenElement {

	//11.	Delete the given element from array.
	public static void main(String[] args) {
		int[] arr = { 25, 14, 56, 15, 36, 56, 77, 18, 29, 49 };
		int newArr[] = new int[arr.length-1];
		int givenElement = 36;
		
		for(int i=0 , j=0; i< arr.length ; i++) {
			if(arr[i] == 36 ) {
				continue;
			}
			newArr[j] = arr[i];
			j++;
		}
		System.out.println(Arrays.toString(newArr));
	}
      }

```
**OUTPUT :** [25, 14, 56, 15, 56, 77, 18, 29, 49]
  **[⬆ Back to Top](#table-of-contents)** 
  
15. ### What is a module?


  **[⬆ Back to Top](#table-of-contents)** 
  
 16. ### What is a module?


  **[⬆ Back to Top](#table-of-contents)**
  
17. ### What is a module?


  **[⬆ Back to Top](#table-of-contents)** 
  
18. ### What is a module?


  **[⬆ Back to Top](#table-of-contents)**
  
19. ### What is a module?


  **[⬆ Back to Top](#table-of-contents)**
  
20. ### What is a module?


  **[⬆ Back to Top](#table-of-contents)**   

21. ### What is a module?


  **[⬆ Back to Top](#table-of-contents)** 

22. ### What is a module?


  **[⬆ Back to Top](#table-of-contents)**   
  
  
  




