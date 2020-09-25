import java.util.Scanner;

public class main {
    public static void main(String[] args) {
        Scanner leer = new Scanner(System.in);
        char r = 's';
        int numero = 0,contador=0;

        operaciones op = new operaciones();


        while (r == 's' && numero != 5) {
            System.out.println("*********************************************************************************");
            System.out.println("Elija una opcion \n1: sumar\n2:Restar\n3:multiplicar\n4:dividir\n5: salir");
            numero = leer.nextInt();
            switch (numero) {
                case 1:
                    double a, b;
                    System.out.println("Ingrese el numero 1");
                    a = leer.nextDouble();
                    System.out.println("Ingresa el numero2");
                    b = leer.nextDouble();
                    System.out.println("El resultado es: " + op.suma(a, b));
                    contador++;
                    break;
                case 2:
                    System.out.println("Ingrese el numero 1");
                    a = leer.nextDouble();
                    System.out.println("Ingresa el numero2");
                    b = leer.nextDouble();
                    System.out.println("El resultado es: " + op.resta(a, b));
                    contador++;
                    break;
                case 3:
                    System.out.println("Ingrese el numero 1");
                    a = leer.nextDouble();
                    System.out.println("Ingresa el numero2");
                    b = leer.nextDouble();
                    System.out.println("El resultado es: " + op.mul(a, b));
                    contador++;
                    break;
                case 4:
                    System.out.println("Ingrese el numero 1");
                    a = leer.nextDouble();
                    System.out.println("Ingresa el numero2");
                    b = leer.nextDouble();
                    System.out.println("El resultado es: " + op.div(a, b));
                    contador++;
                    break;
                case 5:
                    System.out.println("");
                    break;
                default:
                    System.out.println("Ingrese un numero valido");
            }
            if (numero != 5) {
                System.out.println("******************************************************************************");
                System.out.println("¿Desea continuar?\nsi \nno");
                r = leer.next().charAt(0);
            } else {
                System.out.println("Saliendo");
            }
        }
        System.out.println("Operaciones realizadas: "+contador);

        System.out.println("**********************************************************************************");
        System.out.println("Bye");

    }
}
