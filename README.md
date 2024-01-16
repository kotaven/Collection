import java.util.ArrayList;
import java.util.Collections;
import java.util.Iterator;
import java.util.ListIterator;
public class ArrayListEx1 {
	public static void main(String[] args) {
	    ArrayList<String> fruits = new ArrayList<>();
	    fruits.add("apple");
	    fruits.add("banana");
	    fruits.add("cherry");
	    System.out.println(fruits);
	    System.out.println(fruits.contains("apple"));
	    System.out.println("Size of the ArrayList: " + fruits.size());
	    fruits.add(1, "Orange");
	    System.out.println("after orange insert in index 1: "+fruits);
	    fruits.add("orange");  // This is a duplicate
	    fruits.add(null);     // This is a null value
	    System.out.println(fruits);
	    System.out.println("after insert duplicate and null values: "+fruits);
	    String firstFruit = fruits.get(0);
	    String secondFruit = fruits.get(1);
	    String thirdFruit = fruits.get(2);
	    System.out.println("First fruit: " + firstFruit);
	    System.out.println("Second fruit: " + secondFruit);
	    System.out.println("Third fruit: " + thirdFruit);
	    System.out.println("forth fruit: " + fruits.get(3));
	    System.out.println(fruits);
	    fruits.set(0, "apple1");
	    fruits.set(1, "orange1");
	    fruits.set(2, "banana1");
	    System.out.println("Updated ArrayList: " + fruits);
	    fruits.remove(5);
	    System.out.println("After remove(5): " + fruits);
	    boolean isRemoved = fruits.remove("cherry");
	    fruits.remove("cherry");
	    System.out.println("after removing the object cherry: "+fruits);
	    ArrayList<String> fruits1 = new ArrayList<>();
	    fruits1.add("banana1");
	    fruits1.add("orange");
	    System.out.println("after removeAll elemenet: "+fruits.removeAll(fruits1));
	    System.out.println(fruits);
	    System.out.println("Size of the ArrayList: " + fruits.size());
	    System.out.println("after Using Traditional for loop: ");
	    for(int i=0; i < fruits.size(); i++) {
	    	  System.out.println(fruits.get(i));
	    	}
	    System.out.println("after Using Enhanced for loop: ");
	    for(String item : fruits) {
	    	  System.out.println(item);
	    	}
	    System.out.println("after using iterator:");
	    Iterator<String> it = fruits.iterator();
	    while(it.hasNext()) {
	      System.out.println(it.next());
	    }
	    System.out.println("after Using ListIterator (which can iterate in both direction)");
	    ListIterator<String> lit = fruits.listIterator(fruits.size());
	    while(lit.hasPrevious()) {
	      System.out.println(lit.previous());
	    }
	    System.out.println("after Using forEach() method with Lambda expression");
	    fruits.forEach(item -> System.out.println(item));
	    System.out.println("after sort");
	    Collections.sort(fruits);
        System.out.println("Sorted in Ascending order: " + fruits);
        Collections.sort(fruits, Collections.reverseOrder());
        System.out.println("Sorted in Descending order: " + fruits);
}
}
