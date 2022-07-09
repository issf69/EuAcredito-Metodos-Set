# EuAcredito-Metodos-Set
Trabalhando com Collections Java Conhecendo os métodos Set
## package euacredito.com.br;


import java.util.*;

public class ExemploSet {
    public static void main(String[] args) {
// Dada uma lista com 7 notas de um aluno [7, 8.5, 9.3, 5, 7, 0, 3.6], faça:

//      Set notas = new HashSet(); //antes do java 5
//      HashSet<Double> notas = new HashSet<>();
//      Set<Double> notas = new HashSet<>(); //Generics(jdk 5) - Diamont Operator(jdk 7)
/*      Set<Double> notas = Set.of(7d, 8.5, 9.3, 5d, 7d, 0d, 3.6);
        notas.add(1d);
        notas.remove(5d);
        System.out.println(notas);
*/

        System.out.println("Crie um conjunto e adicione as notas: ");
        Set<Double> notas = new HashSet<>(Arrays.asList(7d, 8.5, 9.3, 5d, 7d, 0d, 3.6));
        System.out.println(notas.toString());

//        System.out.println("Exiba a posição da nota 5.0: ");

//        System.out.println("Adicione na lista a nota 8.0 na posição 4: ");

//        System.out.println("Substitua a nota 5.0 pela nota 6.0: ");

        System.out.println("Confira se a nota 5.0 esta no conjunto: " + notas.contains(5d));

//        System.out.println("Exiba a terceira nota adicionada: ");

        System.out.println("Exiba a menor nota: " + Collections.min(notas));

        System.out.println("Exiba a maior nota: " + Collections.max(notas));

        Iterator<Double> iterator = notas.iterator();
        Double soma = 0.0;
        while(iterator.hasNext()) {
            Double next = iterator.next();
            soma += next;
        }
        System.out.println("Exiba a soma dos valores: " + soma);

        System.out.println("Exiba a media das notas: " + (soma/ notas.size()));

        System.out.println("Remova a nota 0: ");
        notas.remove(0d);
        System.out.println(notas);

//        System.out.println("Remova a nota da posição 0");

        System.out.println("Remova as notas menores que 7 e exiba a lista: ");
        Iterator<Double> iterator1 = notas.iterator();
        while(iterator1.hasNext()){
            Double next = iterator1.next();
            if (next < 7) iterator1.remove();
        }
        System.out.println(notas);

        System.out.println("Exiba todas as notas na ordem em que foram informados: ");
        Set<Double> notas2 = new LinkedHashSet<>();
        notas2.add(7d);
        notas2.add(8.5);
        notas2.add(9.3);
        notas2.add(5d);
        notas2.add(7d);
        notas2.add(0d);
        notas2.add(3.6);
        System.out.println(notas2);

        System.out.println("Exiba todas as notas na ordem crescente: ");
        Set<Double> notas3 = new TreeSet<>(notas2);
        System.out.println(notas3);

        System.out.println("Apague todo o conjunto");
        notas.clear();

        System.out.println("Confira se o conjunto esta vazio: " + notas.isEmpty());
        System.out.println("Confira se o conjunto 2 esta vazio: " + notas2.isEmpty());
        System.out.println("Confira se o conjunto 3 esta vazio: " + notas3.isEmpty());

    }
}
###  C:\Users\Irene\.jdks\openjdk-18.0.1.1\bin\java.exe "-javaagent:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.1.1\lib\idea_rt.jar=56245:C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2022.1.1\bin" -Dfile.encoding=UTF-8 -classpath "C:\Users\Irene\Meus Documentos\Conhecendo-os-Metodos-Set\out\production\Conhecendo-os-Metodos-Set" euacredito.com.br.ExemploSet
Crie um conjunto e adicione as notas: 
[0.0, 8.5, 3.6, 5.0, 9.3, 7.0]
Confira se a nota 5.0 esta no conjunto: true
Exiba a menor nota: 0.0
Exiba a maior nota: 9.3
Exiba a soma dos valores: 33.400000000000006
Exiba a media das notas: 5.566666666666667
Remova a nota 0: 
[8.5, 3.6, 5.0, 9.3, 7.0]
Remova as notas menores que 7 e exiba a lista: 
[8.5, 9.3, 7.0]
Exiba todas as notas na ordem em que foram informados: 
[7.0, 8.5, 9.3, 5.0, 0.0, 3.6]
Exiba todas as notas na ordem crescente: 
[0.0, 3.6, 5.0, 7.0, 8.5, 9.3]
Apague todo o conjunto
Confira se o conjunto esta vazio: true
Confira se o conjunto 2 esta vazio: false
Confira se o conjunto 3 esta vazio: false

Process finished with exit code 0
