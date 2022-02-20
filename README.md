package application;

import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;

public class Program {

	public static void main(String[] args) {

		List<Integer> myInts = Arrays.asList(1, 2, 3, 4);
		List<Double> myDoubles = Arrays.asList(3.14, 6.28);
		List<Object> myObjs = new ArrayList<Object>();

		copy(myInts, myObjs);
		printList(myObjs);
		copy(myDoubles, myObjs);
		printList(myObjs);
	}

	/*
	 * (List<de qualquer tipo que extends Number> é a lista de origem,
	 * List<de qualquer tipo que pode ser um super tipo de Number> destino){
	 */
	public static void copy(List<? extends Number> source, List<? super Number> destiny) {
		for (Number number : source) {
			/*
			 * para cada Number number na lista de(:) origem(source)
			 */
			destiny.add(number);
		}
	}
	public static void printList(List<?> list) {
		for (Object obj : list) {
			System.out.print(obj + " ");
		}
		System.out.println();
	}
}

![get-put](https://user-images.githubusercontent.com/61166475/154862247-d73d3457-be6b-4ec7-99df-a066363d99d4.png)
