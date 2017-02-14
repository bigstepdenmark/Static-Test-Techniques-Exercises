# Static Test Techniques Exercise

Triangle opgave: [Klik her](https://github.com/bigstepdenmark/TestExercise1-Triangle)
---

### 1. Static Code Analysis of Triangle program

- 1.b) Check coding standards in your Triangle program

_Klik på screenshot for fuld størrelse_

![alt tag](https://raw.githubusercontent.com/bigstepdenmark/Static-Test-Techniques-Exercises/master/Skærmbillede%202017-02-14%20kl.%2015.48.20.png)

---

- 1.c) Calculate central metrics in your Triangle program

_Klik på screenshot for fuld størrelse_

![alt tag](https://raw.githubusercontent.com/bigstepdenmark/Static-Test-Techniques-Exercises/master/Skærmbillede%202017-02-14%20kl.%2014.50.15.png)

![alt tag](https://raw.githubusercontent.com/bigstepdenmark/Static-Test-Techniques-Exercises/master/Skærmbillede%202017-02-14%20kl.%2016.36.20.png)

![alt tag](https://raw.githubusercontent.com/bigstepdenmark/Static-Test-Techniques-Exercises/master/CC%20by%20method.png)

---

### 2. Peer Review of your Triangle program

Jeg har byttet kode med [Mazlum Dogan Sert](https://github.com/Mazlumsert1/Week-1-Test-Execise)

**Kommentarer:**
Du kunne godt skrive mere kommentarer til dine metoder. Dine controller metoder, synes jeg er lidt for lange, måske skulle du gøre dem mindre, og dermed give mindre ansvar for metoderne.

Triangle.class 

_Private attribute :)_
```java
public class Triangle {

    int a,b,c;

    public Triangle(int a, int b, int c) {
        this.a = a;
        this.b = b;
        this.c = c;
    }
```

TriangleController.class

_Burde de ikke være Private metoder ?_
```java
public boolean isAValidTriangle(int a, int b, int c){
       return (a+b>c && a+c>b && b+c>a);
   }
   
   public boolean validInputs(int a, int b, int c){
        return (a>0 && b>0 && c>0);
    }
```

TriangleMain.class

_Du ville spare linjer, hvis du havde lavet en loop :)_
```java
        System.out.println("Side 1:");
        int a = scan.nextInt();
        System.out.println("Side 2:");
        int b = scan.nextInt();
        System.out.println("Side 3:");
        int c = scan.nextInt();
```
   
---

### 3. Coding Standard Document

- 3.a) Create a coding standard document that describes the best practices and code conventions that you find most important for a team to follow.

For at sikre en udviklingsprojekt sammen med et team, er der nogle standarder der skal opfølges.

**1. Kode kommentarer**

_Det er vigtigt at udvikler skriver kommentarer til metoder. Kommentarer skal stå ovenfor oprationen, altså på sin egen linje. Kommentarerne skal holdes korte, men stadig nemt at forstå._

**2. Navngivning**

Navngivning er yderst vigtig og skal være meningsfulde. I Java skal man som standard følge Java Coding konvention, som er

_Klasser navne skal starte med stor bokstav og følgende camelCase._

_Både Metoder og attributter skal starte med små bokstav og følgende camelCase._

**3. Fejlhåndtering**

I Java vil compileren straks fange exceptions, derfor er det vigtigt at udvikler håndtere fejl ved at anvende try & catch blokke. 
