# Arrays-And-ArrayLists-Demo
Here you will find demo illustrations of Arrays and ArrayLists
// Import necessary classes for ArrayList
import java.util.ArrayList;
import java.util.Arrays; // For utility methods like Arrays.toString()

public class ArrayAndArrayListDemo {

    public static void main(String[] args) {

        // --- Demonstrating Arrays ---
        System.out.println("--- Demonstrating Java Arrays ---");

        // 1. Declaration and Initialization of an Array
        // An array has a fixed size defined at creation.
        // Here, an array of 5 integers is created.
        int[] numbers = new int[5];

        // 2. Assigning values to array elements
        numbers[0] = 10;
        numbers[1] = 20;
        numbers[2] = 30;
        numbers[3] = 40;
        numbers[4] = 50;
        // numbers[5] = 60; // This would cause an ArrayIndexOutOfBoundsException at runtime

        // 3. Accessing array elements
        System.out.println("Element at index 0: " + numbers[0]);
        System.out.println("Element at index 3: " + numbers[3]);

        // 4. Iterating through an array using a for loop
        System.out.print("All elements in 'numbers' array: ");
        for (int i = 0; i < numbers.length; i++) {
            System.out.print(numbers[i] + " ");
        }
        System.out.println(); // New line for better formatting

        // 5. Iterating through an array using a for-each loop (enhanced for loop)
        System.out.print("All elements using for-each: ");
        for (int num : numbers) {
            System.out.print(num + " ");
        }
        System.out.println();

        // 6. Another way to initialize an array (inline)
        String[] fruits = {"Apple", "Banana", "Cherry", "Date"};
        System.out.println("Fruits array: " + Arrays.toString(fruits));
        System.out.println("Size of fruits array: " + fruits.length);

        System.out.println("\n--- Demonstrating Java ArrayLists ---");

        // --- Demonstrating ArrayLists ---
        // 1. Declaration and Initialization of an ArrayList
        // ArrayLists are dynamic in size and can grow or shrink.
        // They store objects, so we use wrapper classes for primitive types (e.g., Integer for int).
        ArrayList<String> colors = new ArrayList<>();

        // 2. Adding elements to an ArrayList
        colors.add("Red");
        colors.add("Green");
        colors.add("Blue");
        colors.add("Yellow");
        colors.add("Purple");

        // 3. Accessing elements from an ArrayList
        System.out.println("First color: " + colors.get(0));
        System.out.println("Third color: " + colors.get(2));

        // 4. Getting the size of an ArrayList
        System.out.println("Number of colors: " + colors.size());

        // 5. Iterating through an ArrayList using a for loop
        System.out.print("All elements in 'colors' ArrayList: ");
        for (int i = 0; i < colors.size(); i++) {
            System.out.print(colors.get(i) + " ");
        }
        System.out.println();

        // 6. Iterating through an ArrayList using a for-each loop
        System.out.print("All elements using for-each: ");
        for (String color : colors) {
            System.out.print(color + " ");
        }
        System.out.println();

        // 7. Removing elements from an ArrayList
        colors.remove("Green"); // Removes by value
        System.out.println("Colors after removing 'Green': " + colors);

        colors.remove(0); // Removes by index (removes "Red" which is now at index 0)
        System.out.println("Colors after removing element at index 0: " + colors);

        // 8. Checking if an element exists
        System.out.println("Does 'Blue' exist? " + colors.contains("Blue"));
        System.out.println("Does 'Green' exist? " + colors.contains("Green"));

        // 9. Clearing all elements from an ArrayList
        colors.clear();
        System.out.println("Colors after clearing: " + colors);
        System.out.println("Is colors ArrayList empty? " + colors.isEmpty());
    }
}
