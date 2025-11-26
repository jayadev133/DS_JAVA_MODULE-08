# Ex11 Convert HashSet to ArrayList in Java
## DATE:20-11-2025
## AIM:
To convert a collection of distinct integers stored in a HashSet into an ArrayList and display its contents.
## Algorithm
1.Start and create an empty HashSet.

2.Insert all the required integers into the HashSet.

3.Create an ArrayList and pass the HashSet to its constructor.

4.Store all elements of the HashSet into the ArrayList.

5.Display the elements of the ArrayList.   

## Program:
```
/*
Program to To convert a collection of distinct integers stored in a HashSet into an ArrayList and display its contents.
Developed by: JAYADEV PALLINTI
RegisterNumber:  212223240058
*/
import java.util.*;

public class HashSetToArrayList {
    public static void main(String[] args) {

        // Create a HashSet of integers
        HashSet<Integer> numberSet = new HashSet<>();

        Scanner sc = new Scanner(System.in);
        System.out.print("Enter how many numbers you want to add: ");
        int n = sc.nextInt();

        // Taking input from the user
        System.out.println("Enter " + n + " distinct integers:");
        for (int i = 0; i < n; i++) {
            numberSet.add(sc.nextInt());
        }

        // Convert HashSet to ArrayList
        ArrayList<Integer> numberList = new ArrayList<>(numberSet);

        // Display the ArrayList
        System.out.println("\nArrayList contents:");
        for (int num : numberList) {
            System.out.println(num);
        }

        sc.close();
    }
}
  
*/
```

## Output:

<img width="623" height="513" alt="image" src="https://github.com/user-attachments/assets/cd6ac697-17cb-4bc7-8fbb-13c23a12f6cf" />


## Result:
The program successfully converts a collection of distinct integers stored in a HashSet into an ArrayList


# Ex12 Add Elements from an Array into a TreeSet
## DATE:20-11-2025
## AIM:
To write a Java program that adds elements from an array into a TreeSet and displays the elements in sorted order.
## Algorithm
1. Start the program.
2. Initialize an array with integer elements.
3. Create an empty TreeSet.
4. Add all elements from the array into the TreeSet.
5. Display the elements of the TreeSet (which are automatically sorted).
6. Stop the program.
   

## Program:
```
/*
Program that adds elements from an array into a TreeSet and displays the elements in sorted order.
Developed by: JAYADEV PALLINTI
RegisterNumber: 212223240058
*/
import java.util.*;

public class ArrayToTreeSet {
    public static void main(String[] args) {
        Integer[] arr = {50, 20, 40, 10, 30};

        TreeSet<Integer> set = new TreeSet<>(Arrays.asList(arr));

        System.out.println("Array elements: " + Arrays.toString(arr));
        System.out.println("TreeSet elements (sorted): " + set);
    }
}
 
*/
```

## Output:

<img width="446" height="65" alt="image" src="https://github.com/user-attachments/assets/42b2a190-23fa-4210-87b2-89a7e7458b27" />


## Result:
The program successfully adds elements from an array into a TreeSet.

# Ex13 Fill the First 10 Elements of an Array with a Constant using Arrays.fill()
## DATE: 20-11-2025
## AIM:
To write a Java program that fills the first 10 elements of an array with a constant value using the Arrays.fill() method.
## Algorithm
1. Start the program.
2. Create an integer array of size 10.
3. Use Arrays.fill() to assign a constant value to all 10 elements.
4. Print the array elements using Arrays.toString().
5. End the program.
 

## Program:
```
/*
Program to FILL the first 10 elements of an array with a constant value using the Arrays.fill() method.
Developed by: JAYADEV PALLINTI
RegisterNumber: 212223240058
*/
import java.util.Arrays;

public class FillArray {
    public static void main(String[] args) {
        int[] arr = new int[10];
        Arrays.fill(arr, 5);
        System.out.println("Array after filling: " + Arrays.toString(arr));
    }
}
*/
```

## Output:

<img width="477" height="54" alt="image" src="https://github.com/user-attachments/assets/df1870c0-8949-4e78-9c6f-28cc4f6310d8" />


## Result:
The program successfully fills the first 10 elements of the array with the constant value 5 using the Arrays.fill() method.

# Ex14 Tracking the First Unique Number in a Stream using LinkedHashMap
## DATE:20-11-2025
## AIM:
To implement a program that tracks the first unique (non-repeating) number in a stream of integers using a LinkedHashMap.

## Algorithm
1. Start the program.
2. Create a LinkedHashMap to store numbers and their frequency counts.
3. For each incoming number in the stream:
    =>Increment its count in the map.
4. Iterate through the map to find the first number with a count of 1.
5. Display the first unique number.
6. Stop the program.
   

## Program:
```
/*
Program to track the first unique (non-repeating) number in a stream of integers using a LinkedHashMap.
Developed by: JAYADEV PALLINTI
RegisterNumber: 212223240058
*/
import java.util.*;

public class FirstUniqueTracker {
    public static void main(String[] args) {
        int[] stream = {4, 5, 4, 5, 3, 2, 1};
        LinkedHashMap<Integer, Integer> map = new LinkedHashMap<>();

        for (int num : stream)
            map.put(num, map.getOrDefault(num, 0) + 1);

        System.out.println("Stream: " + Arrays.toString(stream));
        for (Map.Entry<Integer, Integer> entry : map.entrySet()) {
            if (entry.getValue() == 1) {
                System.out.println("First unique number: " + entry.getKey());
                return;
            }
        }
        System.out.println("No unique number found.");
    }
}  
*/
```

## Output:


<img width="318" height="71" alt="image" src="https://github.com/user-attachments/assets/cb4172ad-f4f2-4ca7-a537-75e7f8516c30" />

## Result:
The program successfully tracks and returns the first unique number at any point in the integer stream using a LinkedHashMap.


# Ex15 Value Existence Check in a TreeMap
## DATE:20-11-2025
## AIM:
To write a Java program that checks whether a given value exists in a TreeMap.

## Algorithm
1. Start the program.
2. Create a TreeMap and insert key–value pairs.
3. Use the containsValue() method to check if a specific value exists in the map.
4. Display whether the value is found or not.
5. Stop the program.
   

## Program:
```
/*
Program to check whether a given value exists in a TreeMap.
Developed by: JAYADEV PALLINTI
RegisterNumber: 212223240058
*/
import java.util.*;

public class TreeMapValueCheck {
    public static void main(String[] args) {
        TreeMap<Integer, String> map = new TreeMap<>();
        map.put(1, "Apple");
        map.put(2, "Banana");
        map.put(3, "Cherry");
        map.put(4, "Mango");

        System.out.println("TreeMap: " + map);
        String valueToCheck = "Banana";

        if (map.containsValue(valueToCheck))
            System.out.println("The value '" + valueToCheck + "' exists in the TreeMap.");
        else
            System.out.println("The value '" + valueToCheck + "' does not exist in the TreeMap.");
    }
}
*/
```

## Output:

<img width="522" height="72" alt="image" src="https://github.com/user-attachments/assets/40c0a480-8eda-4644-9b37-82529bc7386b" />


## Result:
Thus, the program successfully checks whether a specified value exists in a TreeMap using the containsValue() method.
