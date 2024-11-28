# C# Desde 0

> [!WARNING]
> Esto es un desde 0, solamente de contenido básico.

- Es un lenguaje fuertemente tipado.
- Tiene que compilarse.
- Es un lenguaje medianamente funcional.
- Orientado a objetos.

> [!NOTE]
> Para crear el proyecto se uso `dotnet new console -o ./NOMBRE/`

[Documentación oficial.](https://learn.microsoft.com/es-es/dotnet/csharp/?WT.mc_id=dotnet-35129-website)

## Hola Mundo!

```cs
// Program.cs
Console.WriteLine("Hola Mundo!");
```

Ejecutamos el comando

```sh
dotnet run

# output:
# Hola Mundo!
```

## Variables y Constantes

### Variables

Para declarar una variable se puede hacer de las siguientes formas:

- Sigue el formato de `<tipo> <nombre> = <valor>;`.
  - Esto es util cuando queremos dejar explicitamente el tipo de dato que queremos usar.
- Sigue el formato de `var <nombre> = <valor>;`.
  - Esto nos sirve para hacer que `C#` infiera el tipo de dato que estamos asignando a la variable.
  - Esto se usa principalmente en tipos de datos primitivos.

> [!TIP]
> El nombre por convención es en camelCase.

```cs
string myString = "Hola";
Console.WriteLine(myString);
myString = "Adios";
Console.WriteLine($"Interpolación de texto con variables: {myString}");
```

### Constantes

Para declarar una constante se usa el siguiente formato: `const <tipo> <nombre> = <valor>;`

```cs
const string MyString = "Hola";
Console.WriteLine($"Interpolación de texto con constantes: {MyString}");
```

## Tipos de datos

| Tipo            | Keyword |
| --------------- | ------- |
| Cadena de texto | string  |
| Entero          | int     |
| Decimal         | float   |
| Decimal/Double  | double  |
| Booleano        | bool    |
| Dinamico        | dynamic |

## Esctructuras

### Arreglos / Array

```cs
var myArray = new string[] { "Test 1", "Test 2", "Test 3" };
Console.WriteLine(myArray); // System.String[]
Console.WriteLine(myArray[0]); // Test 1

myArray[1] = "Test 2!"; // Sobreescribimos el valor del index 1
Console.WriteLine(myArray[1]); // Test 2!
```

### Diccionarios

```cs
// Esto es                         clave, valor
var myDictionary = new Dictionary<string, int>
{
    {"Test 1", 0},
    {"Test 2", 1},
    {"Test 3", 2}
};
Console.WriteLine(myDictionary["Test 1"]); // 0
```

### HashSet

La peculiaridad de los `HashSet` es que:

1. No son ordenados.
2. Los datos repetidos son obviados y no se muestran mas de 1 vez.

```cs
var mySet = new HashSet<string> { "Test 1", "Test 2", "Test 3", "Test 2" };
```

### Tuplas

```cs
var myTuple = ("Test 1", "Test 2", "Test 3", "Test 2");
Console.WriteLine(myTuple); // (Test 1, Test 2, Test 3, Test 2)
```

## Bucles

### For

```cs
for (int index = 0; index < 10; index++)
{
    Console.WriteLine(index);
}
```

### Foreach

```cs
var mySet = new HashSet<string> { "Test 1", "Test 2", "Test 3", "Test 2" };

foreach (var item in mySet)
{
    Console.WriteLine(item);
}
```

## Flujos

```cs
string myString = "Test";
bool myBool = true;

if (myString == "Test" && myBool == false)
{
    Console.WriteLine("Es Test");
}
else if (myString == "Test" && myBool == true)
{
    Console.WriteLine("My bool es true");
}
else
{
    Console.WriteLine("Test");
}
```

## Funciones

Las funciones se declaran con `<tipo de retorno> <nombre>(){}`

```cs
void MyFunction(int a, int b)
{
    Console.WriteLine(a + b);
}

MyFunction(5, 5); // 10
```

## Clases
