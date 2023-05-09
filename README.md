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
|7 | [Find second largest number in array ?](#Find-second-largest-number-in-array)|
|8 | [What are the differences between Component and Directive?](#what-are-the-differences-between-component-and-directive)|
|9 | [What is a template?](#what-is-a-template)|
|10| [What is a module?](#what-is-a-module)|


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

7. ### Find second largest number in array ?
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

8. ### What are the differences between Component and Directive?
    In a short note, A component(@component) is a directive-with-a-template.

    Some of the major differences are mentioned in a tabular form

    | Component | Directive |
    |---- | ---------
    | To register a component we use @Component meta-data annotation  | To register a directive we use @Directive meta-data annotation |
    | Components are typically used to create UI widgets| Directives are used to add behavior to an existing DOM element |
    | Component is used to break down the application into smaller components| Directive is used to design re-usable components|
    | Only one component can be present per DOM element | Many directives can be used per DOM element |
    | @View decorator or templateurl/template are mandatory | Directive doesn't use View|

  **[⬆ Back to Top](#table-of-contents)**

9. ### What is a template?
    A template is a HTML view where you can display data by binding controls to properties of an Angular component. You can store your component's template in one of two places. You can define it inline using the template property, or you can define the template in a separate HTML file and link to it in the component metadata using the @Component decorator's templateUrl property.

    **Using inline template with template syntax,**
    ```typescript
    import { Component } from '@angular/core';

    @Component ({
       selector: 'my-app',
       template: '
          <div>
             <h1>{{title}}</h1>
             <div>Learn Angular</div>
          </div>
       '
    })

    export class AppComponent {
       title: string = 'Hello World';
    }
    ```
    **Using separate template file such as app.component.html**
    ```typescript
    import { Component } from '@angular/core';

    @Component ({
       selector: 'my-app',
       templateUrl: 'app/app.component.html'
    })

    export class AppComponent {
       title: string = 'Hello World';
    }
    ```

  **[⬆ Back to Top](#table-of-contents)**

10. ### What is a module?

    Modules are logical boundaries in your application and the application is divided into separate modules to separate the functionality of your application.
    Lets take an example of **app.module.ts** root module declared with **@NgModule** decorator as below,
    ```typescript
    import { NgModule }      from '@angular/core';
    import { BrowserModule } from '@angular/platform-browser';
    import { AppComponent }  from './app.component';

    @NgModule ({
       imports:      [ BrowserModule ],
       declarations: [ AppComponent ],
       bootstrap:    [ AppComponent ],
       providers: []
    })
    export class AppModule { }
    ```
    The NgModule decorator has five important (among all) options:
    1. The imports option is used to import other dependent modules. The BrowserModule is required by default for any web based angular application.
    2. The declarations option is used to define components in the respective module.
    3. The bootstrap option tells Angular which Component to bootstrap in the application.
    4. The providers option is used to configure a set of injectable objects that are available in the injector of this module.
    5. The entryComponents option is a set of components dynamically loaded into the view.

  **[⬆ Back to Top](#table-of-contents)**




