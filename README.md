# tarea-temperatura-java
conversor_temperatura.java
/*
 * Programa: Conversor de Temperatura
 * Funcionalidad: Convierte una temperatura de grados Celsius a Fahrenheit y Kelvin.
 */

import java.util.Scanner;

public class conversor_temperatura {

    public static void main(String[] args) {
        // Crear objeto Scanner para leer entrada del usuario
        Scanner entrada_usuario = new Scanner(System.in);

        // Solicitar al usuario la temperatura en Celsius
        System.out.print("Ingresa la temperatura en °C: ");
        // Utilizamos float para admitir decimales
        float temperatura_celsius = entrada_usuario.nextFloat();

        // Convertir a Fahrenheit: (°C × 9/5) + 32
        float temperatura_fahrenheit = convertir_a_fahrenheit(temperatura_celsius);

        // Convertir a Kelvin: °C + 273.15
        float temperatura_kelvin = convertir_a_kelvin(temperatura_celsius);

        // Mostrar resultados
        System.out.printf("Temperatura en Fahrenheit: %.2f °F%n", temperatura_fahrenheit);
        System.out.printf("Temperatura en Kelvin: %.2f K%n", temperatura_kelvin);

        // Cerrar scanner
        entrada_usuario.close();
    }

    // Función para conversión a Fahrenheit
    public static float convertir_a_fahrenheit(float celsius) {
        return (celsius * 9 / 5) + 32;
    }

    // Función para conversión a Kelvin
    public static float convertir_a_kelvin(float celsius) {
        return celsius + 273.15f;
    }
}
