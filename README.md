# Parsear:

Lo correcto:

    sout"Ingrese un valor"
    String valorStr = scanner.nextLine()
    int valor = Integer.parseInt(valorStr)

# División de números:

entero/entero = entero
float divConDecimales = (1.0f * num1) / num2
    
# Lista de algunas excepciones:

Dividir entre cero:

    ArithmeticException

Acceder a una ubicacion incorrecta de un arrreglo:

    ArrayIndexOutOfBoundsException

Parsear a entero un String que es una letra:

    NumerFormatException

Usar un objeto, el cual su atributo no fue dado o instanciado:

    NullPointerException

# Ver excepciones:
crtl + Q

throws .......(la excepcion)

# Try - catch - finally:
Es necesario declarar la variable antes de que este en el try:
TipoDeDato NombreVariable;

    sout("Eliga un opcion (1,2,3): ");
    String opcionStr = sc.nextLine();
    
    int opcion;
    try{
        int opcion = Integer.parseInt(opcionStr)
    }catch(NumberFormatException e){
        sout("El numero recibido no es un entero")
        opcion = -1; //podemos poner en un switch que cuando opcion es -1 es un error
    }

-------------------------------------

    System.out.println("División de 2 números enteros");
    
    int num1;
    int num2;
    
    buc1:
    while (true) {
        System.out.print("Número 1:");
        String num1str = sc.nextLine();
    
        try {
            num1 = Integer.parseInt(num1str);
            break buc1;
        } catch (NumberFormatException e) {
            System.out.println("El número ingresado no es un entero");
        }
    }

    buc2:
    while (true) {
        System.out.print("Número 2:");
        String num2str = sc.nextLine();
        try {
            num2 = Integer.parseInt(num2str);
            if (num2 == 0) {
                System.out.println("No puede dividir entre 0");
                continue buc2; // de aqui se va de frente al while true buc 2 de nuevo, no llega al break buc2
            }
            break buc2;
        } catch (NumberFormatException e) {
            System.out.println("El número ingresado no es un entero");
        }
    }
    
    float div = (1.0f * num1) / num2;
    
    System.out.println("El resultado es: " + div);

## Multiples catch:

![image](https://github.com/Pierohc/Java-Excepciones/assets/133154904/94faf6a6-d292-48f3-bb0e-f7622b69f417)

Se debe considerar que en el catch hay prioridades. Se debe poner primero la excepcion mas específica y luego la más general. Por lo que los errores no deben capturarse, si no que estos deben corregirse.

![image](https://github.com/Pierohc/Java-Excepciones/assets/133154904/087628f0-6ac3-400c-89ee-749e63b48e65)


Por lo que algo general, ya que todas las excepciones heredan de la clase Exception, sería (No recomendable de usar): 

![image](https://github.com/Pierohc/Java-Excepciones/assets/133154904/e86db745-a022-4096-b369-09db911ebdbc)


--------------------

Otra forma si no importa saber que excepción se ejecutará: 

![image](https://github.com/Pierohc/Java-Excepciones/assets/133154904/bf57f2cb-272c-48a9-a35a-7a8264f46ecb)


----------------

## Tipos de excepciones:
![image](https://github.com/Pierohc/Java-Excepciones/assets/133154904/8bd8b949-8382-45db-8600-82dc845e18f5)

-------
# OJO:
Creamos un metodo en una clase diferente al MAIN:
![image](https://github.com/Pierohc/Java-Excepciones/assets/133154904/4ba58949-ec03-4e90-a0ea-9d46e198daa1)


## Crear mis propias excepciones:





