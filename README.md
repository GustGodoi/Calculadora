# Calculadora

package Calculadora;

import Operação.OperacoesAvancadas;
import Operação.OperacoesBasicas;
import java.util.Scanner;

public class Calculadora {

    public static void main(String[] args) {
        
        OperacoesBasicas op = new OperacoesBasicas();
        OperacoesAvancadas opA = new OperacoesAvancadas();
        Scanner leia = new Scanner(System.in);
        
        System.out.println("Informe o primeiro número: ");
        double num1 = leia.nextDouble();
        System.out.println("Informe o segundo número: ");
        double num2 = leia.nextDouble();
        System.out.println("informe a operação: "+" | "+"+"+" | "+"-"+" | "+"/"+" | "+"*"+" | "+"!"+" | ");
        String operacao = leia.next();
        
        if(operacao.equals("+")){
            double resultado = op.somar(num1, num2);
            System.out.println(resultado);
        }
        if(operacao.equals("-")){
            double resultado = op.subtrair(num1, num2);
            System.out.println(resultado);
        }
        if(operacao.equals("/")){
            double resultado = op.dividir(num1, num2);
            System.out.println(resultado);
        }
        if(operacao.equals("*")){
            double resultado = op.multiplicar(num1, num2);
            System.out.println(resultado);
        }
        if(operacao.equals("!")){
            double resultado = opA.potenciacao(num1, num2);
            System.out.println(resultado);
        }
        
    }
    
}


//OPERAÇÕES BÁSICAS:

package Operação;

public class OperacoesBasicas {

    public double somar(double a, double b) {
        double resultado = a + b;
        return resultado;
    }

    public double subtrair(double a, double b) {
        double resultado = a - b;
        return resultado;
    }

    public double dividir(double a, double b) {
        double resultado = a / b;
        return resultado;
    }

    public double multiplicar(double a, double b) {
        double resultado = a * b;
        return resultado;
    }
}

//OPERAÇÕES AVANÇADAS:


package Operação;

public class OperacoesAvancadas {
    public double potenciacao(double base, double potencia){
        
        double resultado = 1;
        
        
        for (int i = 0; i < potencia; i++) {
            resultado = base * resultado;
        }
            
        return resultado;
    }
        
}
