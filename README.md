package application;

import java.util.ArrayList;
import java.util.List;

public class Program {

	public static void main(String[] args) {

		List<Object> myObjs = new ArrayList<Object>();
		
		myObjs.add("Maria");
		myObjs.add("Alex");
		
		
		/*
		 * contravariancia
		 * eu vou declarar uma lista myNums do tipo <qualquer<?> tipo super Number>, ou seja, pode ser um Number ou
		 * qualquer superTipo de Number, no caso aqui, o superTipo de Number é o Object, então essa minha lista myNums aqui
		 * pode ser tanto Number como Object, então nessa adicionar qualquer valor que seja do tipo Number, que aqui por ex
		 * foi do tipo int(linha28) ou double(linha29), ou tambem objetos de um superTipo de number, eu posso adicionar aqui
		 * String, e posso adicionar aqui por ex Objetos Object, só que agora eu vou ter o contrario, eu não posso acessar
		 * os objetos da lista, porem a operação de inserir é permitida, pq? porque o tipo dessa lista pode ser um tipo
		 * que seja um super tipo de Number, então essa atribuição não pode ser feita para uma variavel Number.
		 */
		List<? super Number> myNums = myObjs;
		
		myNums.add(10);
		myNums.add(3.14);
		
		Number x = myNums.get(0);
	}
}

![get-put_ contravariancia](https://user-images.githubusercontent.com/61166475/154862273-133ba729-f221-4f89-8fee-0e278a1199a7.png)
