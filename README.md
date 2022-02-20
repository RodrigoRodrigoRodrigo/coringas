package application;

import java.util.ArrayList;
import java.util.List;

public class Program {

	public static void main(String[] args) {

		List<Integer> intList = new ArrayList<Integer>();
		intList.add(10);
		intList.add(5);
		
		List<? extends Number> list = intList;
		
		/*
		 * convariancia é quando o deixa eu acessar os elementos, linha 21.
		 * mas NÃO deixa eu adicionar, ele da um erro ao adicionar, linha 23.
		 * 
		 * isso se chama covariancia, quando a operação de get é permitida
		 * só que a operação de inserir ela não é permitida.
		 */
		
		Number x = list.get(0);
		
		list.add(20);

	}
}

![get-put_covariancia](https://user-images.githubusercontent.com/61166475/154862283-ca21ead4-7b77-49ac-b81e-860d4dfc7644.png)
