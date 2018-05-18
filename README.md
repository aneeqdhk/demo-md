# Array of Objects

We have already seen how Arrays are very useful in keeping the same type of data together. Let's see how arrays can be used with Objects.

## Why Arrays?

Let's go back to the example of our `Boy` class. Let's say we want to define a classroom of 10 boys. Without arrays, this is how we would do it:

```Java
class Boy{
    String clothes; //instance-variables
    String mood;
    int current_speed;
    
    public void run(){
        //defining run method
    }

    public void jump(){
        //defining jump method
    }
}


public class Main{
    public static void main(String[] args){
        Boy boy_1 = new Boy();        
        Boy boy_2 = new Boy();
        Boy boy_3 = new Boy();
        Boy boy_4 = new Boy();
        Boy boy_5 = new Boy();
        Boy boy_6 = new Boy();
        Boy boy_7 = new Boy();
        Boy boy_8 = new Boy();
        Boy boy_9 = new Boy();
        Boy boy_10 = new Boy();        
    }
}
```
As you can see, there is a lot of code: and we haven't even given any values to the objects!

We can make this process much better, with the help of arrays.

## How to create an Array of Objects

Arrays of Objects are ***different*** from the typical array we have seen. Let's understand how they are different.

Look at the following code:

```Java
public class Main{
    public static void main(String[] args){
        Boy[] boy_array = new Boy[10];
    }
}
```

What happened here?

An array called `boy_array` has been created. It has 10 elements. What are these elements? The elements of this array are ***NOT OBJECTS***. The elements of this array are ***reference variables***.

And initially, all these reference variables are `null` because we have not created any new objects!

Our array looks like this right now:

![null array](https://blockly.netlify.com/static/array_objects_1.png)

---

For these references to point to objects, we need to create new objects.

Do you remember the syntax for creating new objects? An example from the previous topic:

```Java
public class Main{
    public static void main(String[] args){
        Boy boy_1; //defining the reference
        boy_1 = new Boy(); // new object created

        boy_1.clothes = "Summer"; //accessing the instance variables
        boy_1.mood = "Happy";
        boy_1.current_speed = 0;
    }
}
```

To assign an object, to a reference, we need to use the syntax `new Boy()`.

Let us do that, with our array:

```Java
public class Main{
    public static void main(String[] args){
        Boy[] boy_array = new Boy[10];
        boy_array[0] = new Boy();
        boy_array[1] = new Boy();
        boy_array[2] = new Boy();
        boy_array[3] = new Boy();
        boy_array[4] = new Boy();
        boy_array[5] = new Boy();
        boy_array[6] = new Boy();
        boy_array[7] = new Boy();
        boy_array[8] = new Boy();
        boy_array[9] = new Boy();
    }
}
```

> Remember, array indexing begins from `0`!

We are still writing & repeating too many lines of code. Let's use loops to make this better:

```Java
public class Main{
    public static void main(String[] args){
        Boy[] boy_array = new Boy[10];
        for(int i =0; i<boy_array.length; i++)
        {
            boy_array[i] = new Boy();
        }
    }
}
```

Now, our array looks like this:

![default array](https://blockly.netlify.com/static/array_objects_2.png)

### Accessing elements of an Array of Objects

Just like earlier, we can use the `.` operator to access the variables and methods of an object.

Let us create an array of 10 boys, all wearing `Summer` clothes and are in the `Idle` mood.

```Java
public class Main{
    public static void main(String[] args){
        Boy[] boy_array = new Boy[10];
        for(int i =0; i<boy_array.length; i++)
        {
            boy_array[i] = new Boy();
            boy_1[i].clothes = "Summer"; //accessing the instance variables of ith Boy Object
            boy_1[i].mood = "Idle";
        }
    }
}
```

We get the following array:

![objects array](https://blockly.netlify.com/static/array_objects_3.png)


Let us now change the values of the 3rd & 7th boys:


```Java
public class Main{
    public static void main(String[] args){
        Boy[] boy_array = new Boy[10];
        for(int i =0; i<boy_array.length; i++)
        {
            boy_array[i] = new Boy();
            boy_1[i].clothes = "Summer"; //accessing the instance variables of ith Boy Object
            boy_1[i].mood = "Idle";
        }

        boy_array[2].clothes = "Winter"; //Accessing 3rd boy
        boy_array[6].mood = "Happy"; //Accessing 7th boy
    }
}
```

![objects array](https://blockly.netlify.com/static/array_objects_4.png)

Make sure you check as many examples as possible on Arrays & Objects, to understand it better.
