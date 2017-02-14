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
```
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
```
public boolean isAValidTriangle(int a, int b, int c){
       return (a+b>c && a+c>b && b+c>a);
   }
   
   public boolean validInputs(int a, int b, int c){
        return (a>0 && b>0 && c>0);
    }
```

TriangleMain.class

_Du ville spare linjer, hvis du havde lavet en loop :)_
```
        System.out.println("Side 1:");
        int a = scan.nextInt();
        System.out.println("Side 2:");
        int b = scan.nextInt();
        System.out.println("Side 3:");
        int c = scan.nextInt();
```
   
