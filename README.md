# **Java-CS003-Winter Live**

##  :open_file_folder: *Listings and Instructions*
1. Important Words are listed by both **Bold and *Italicized***.
2. This is for absolute beginners having **1 or more month of experience working with Java**.
3. Stay tuned with us on Youtube for quality content and explanation [**Antern**](https://youtube.com/channel/UCIpbqdvNWx50J79KAG1Q21A) and follow Team Antern on LinkedIn for free contents [**LinkedIn**](https://www.linkedin.com/company/team-antern)
4. Go through the **code very carefully** and 
5. The Answers of ****Test Yourself**** is to be written in the **Answers** section on Server.
---
## :bookmark_tabs: *Topics Covered Here*
1. **Identifiers**
    a. [Identifiers](#Sub-topic-A--Identifiers)
    b. [Rules of Identifiers](#Sub-Topic-B-Rules-of-Identifiers-or-Nomenclature)
2. **Datatypes**
    - [What are Datatypes](#What-are-Datatypes?)
    - [Concept of Local Variable Type Inferencing.](#Case-Study-:-Local-Variable-Type-Inferencing)
    a. [byte](#byte)
    b. [short](#short)
    c. [int](#int)
    d. [long](#long)
    e. [float](#float)
    f. [double](#double)
    g. [boolean](#boolean)
    h. [char](#char)
3. **Variables**
    * [Variables.](#Variables)
    * [Identifiers vs Variables.](#Identifier-VS-Variable)
---
## :question: **Frequently Asked Questions(FAQs)**
1. [Even when **char** and **short** have the same size, they have different range.](#Even-when-char-and-short-have-the-same-size,-they-have-different-range.)
2. [Why using **float** is not preferred when dealing with higher floating point values.](##Why-using-float-is-not-preferred-when-dealing-with-higher-floating-point-values)

---

## ***Topic 1: Identifiers***
### **Sub-topic A : Identifiers**

1. Definition: - **Identifiers are names  that are given to an element that identify an element of a program uniquely**
2. What can be an Idenfier in a Java Program?
    - All constants, variables, methods, classes, interfaces, packages, interfaces, enums, etc. can be identified by assigning to them an unique name. This unique name is called Identifier.
 ![](https://i.imgur.com/xPrupXN.jpg)

3. The above image :arrow_up: is of an organism. We identify the organism as a **Human**. Hence *Human* is an identifier since it identifies a specific type of organism uniquely.

4. Why do we need identifiers? 
    - When it comes to real life, you must have heard about Scientific Names of organisms in Biology. 
    - And you must have heard about **Nomenclature**, or the **process of naming an organism uniquely**. 
    - Similarly, so as to tell our Java Virtual Machine that **one element is different from another element of the same type, it is necessary to provide each element an unique name.**
    - ***So as to avoid name-space collisions between two common elements of a program, we mainly use Identifiers.***
    - Eg: Suppose that in a class of 60 students, coincidentally 3 students having the same name namely: Krish Jaiswal. So how would you identify them uniquely? When a teacher calls "Krish Jaiswal", all three stand up. ***Hence they all students have been allotted with Enrollment Numbers and Serial Numbers which is unique for a class. Hence the Enroll no. and Serial no. are identifiers.***
---
### **Sub-Topic B: Rules of Identifiers or Nomenclature**
1. Identifiers **must start with** **$** or **'_'** or **A-Z** or **a-z**. It **must contain** any of these characters listed above. 
2. An Identifier Name ***must be a legit word***.
    Eg: **A person calls his/her water bottle as "Water Bottle" and not a "Bore Well". It is possible to name the water bottle as "Bore Well" but it is not legitimate.** Hence it should be a legitimate word.
3. ***An Identifier can be of any length.***
    Eg: If you have seen the [**Butterflow Pen Ad**](https://youtu.be/bTuvEIyE6Fc), you must have seen a person telling his name which would seem like the names of all persons living in his village. That kind of name is supported in Java but **It is the Worst Programming Practice**. 
4. ***An Identifier cannot be a Keyword or Reserved Word in Java***
    Eg: - 
    ``` Java
        class static{ ... }    // Syntax Error: -
        int yield = 10;         //Syntax Error: -
        int result = 20;        //Absolutely Correct: -
    ```
5. There should be ***NO WHITESPACE*** character in the Identifier. 
    Eg: You cannot have an identifier named **demo 1** for an element in Java.
6. Java is ***case-sensitive***. So if I write **HELLO** and **hello** it means a hell lot of difference.
7. The identifier **must not contain a digit (0-9).**
    Eg: Your name does not contain a digit. 
    ``` Java
        class 123abc{ ... }    //Syntax Error
        int 3A = 10; //Syntax Error
        int A3 = 10;  //200% Correct.
    ```
    
#### Note:
 - It is not possible to remember all the rules. Generally, we just remember our **Name** and make out points from it.
 - Eg: **Name : *Krish Jaiswal*** : *Conclusions Drawn:*
     - The Name **does not begin with any Number or digit**.
     - The Name **may contain upper or lower case** alphabetical characters.
     - Considering **Krish**, there is **no Whitespace** here.
     - Name is **short and sweet**. It is **appropriate**.
---


| Identifier Name | Is It Valid? | Invalid | Reason |
| -------- | -------- | -------- | -------- |
| 123af     | ~~Valid~~     | **It is Invalid**     | **It must not start with a Number** |
| _123     |  **Valid**    | ~~It is Invalid~~ | **Valid since it begins with an underscore ( _ )** |
| $a        | **Valid**    | ~~It is Invalid~~ | **Valid since it begins with a $ symbol** |
| Abc      | **Valid**     | ~~It is Invalid~~| **Valid since it begins with an Aplhabetical Character.**
| 1$221a  | ~~Valid~~ | **It is Invalid** | **Invalid because an identifier cannot begin with a number.**
| _abc   | **Valid**     | ~~It is Invalid~~ | **Valid since it begins with an underscore**
| a bc12 | ~~Valid~~ | **It is Invalid** | **Invalid because it contains a whitespace**
| public | ~~Valid~~ | **It is Invalid** | **Invalid because it is a reserved word in Java**.
---
### ****Sub Topic C: Test Yourself****
1. How many identifiers are present in the below given program. 
    Eg: String is an **identifier**. Hence ***count it only once.***
    ``` Java
    public class Hello{
         public static void main(String[] args){
             String melody = "Why is Melody so Chocolatey";
             String answer = "Eat Melody! And that itself will give you the answer.";
         }   
    }
    ```
2. **Predict** the **first line** where the **error may originate(if any)** and **explain the reason**. : - 
    ``` Java
        public class Demo1{
            public static void main(String[] args){
                int 3_ide = 20.0;    //1
                double d1 = 22_00_3__.323;    //2
                String str = "@Auth Krish";    //3
            }
        }
    ```
3. ***Can we have a deprecated reserved word as an identifier? State the reason for the same.*** 
4. Which is/are a correct identifier/s?
    - [ ] ___dent
    - [ ] _:__dent
    - [ ] dent___
    - [ ] __$_
    - [ ] _transient
    - [ ] goto
5. Explain about ***Identifiers in your own words.***
---
## ****Conclusions****
1. Identifier is a name given to **identify each element in a program uniquely to avoid name-space collisions.**
2. So as to declare a word as Identifier in your program, you **need to follow the Nomenclature of Elements/Rules of using Identifiers.**
3. Identifiers must not be a **reserved word**, **shouldn't begin with a digit**.
4. Using the special character **$** and **_** is allowed.
5. There must not be any **WHITESPACE** in the identifier.
6. Suitable Identifier **must be between 3 to 10 characters long and should define the use by its name itself.**
    Eg: *When writing a program that prints **Hello World**, the class name should be **Hello**.*
---


---
---
## ***Topic 2: Datatypes***
### *What are Datatypes?*
 *Datatypes*: **The type of data a variable can hold is called a Datatype.**
 - Datatypes allow variables to act as a container of a specific type which can store the values of the same specific type.
    Eg: To store liquids, you will use a container or vessel. That vessel may store different volumes of water. But all those vessel will store only liquids.
    - *Hence **Liquid is a type of data a vessel(variable) can hold** and the volume of the vessel is the range/capacity to which the variable can hold the type of data*.
    **- Vessel = Variable**
    **- Volume of Vessel = Range of Datatype**
    **- Liquid = Type of Data.**

Why do we need a Datatype?
- For Example: Let's consider the same example given above. When you know the type of data, it becomes easier for you to choose a vessel. Similarly, when we consider this in Technological Terms, **it becomes easier for the Compiler to choose a variable of convenient size and range.**
- But in the next case, we would see that the Compiler would detect the datatype automatically and would choose the required vessel.
- It **increases the Efficiency of the Program** during Runtime. It is **because the Compiler knows how much memory is to be allocated for each variable of the given type.**
- **It would make a program robust and error free by preventing any kind of incompatible type error.**

### **Case Study : Local Variable Type Inferencing**
- An Interesting thing is to know that with JDK 10, you can use variables without even using datatypes.
- We will very soon learn that **So as to use variables, we ***Must declare the variable prior to its use and it must be initialized with a value and its initializer type.*****
- But, in this case, the Compiler would automatically detect the type of initializer.
- This reduces code redundancy and helps in situations where deciding the type is difficult to make out or cannot be denoted. 
- *Definition*: **Local Variable Type Inferencing is a concept where the Compiler automatically identifies/recognizes the type of data that is to be stored in the variables.**
- It is achieved by using a **context-specific identifier** namely: **var**.
- **var** is context-specific since it depends on the place of the usage in a Java Program. 
- Eg: Let's Consider the Given Example: -
    ``` Java
        public class Foo{
            public static void main(String[] args){
                var i = 10;        //var is an context specific identifier here.
                int var = 10;     //var is an context-indefinite/user-defined identifier here.
            }
        }
    
    ```
    
- ![](https://i.imgur.com/J4ChVbq.png)
- In the above picture, :arrow_up: its visible that **var** acts as a **context-specific identifier**.
- **Definition**: **Context-Specific Identifier means an identifier(not a reserved word) having different functionalities when used at different places in a Java program.**
- Eg: of a program where **var** is an user-defined identifier.
    ``` Java
        public class Demo2{
            public static void main(String[] args){
                int var[] = {1,23,34,2,2,1,2,3};  //Here var is an user defined identifier.
            }
        }
    
    ```
- This Program shown above would not show any error.
- Syntax of User-Defined **var** named Identifier.
- ![](https://i.imgur.com/V7HW1JE.png)

- We would learn more about Local Variable Type Inferencing very soon in another Notes.

---
### **Is Java Statically Typed Language?**
1. The Answer is ***Yes***.
2. **Reasons: -**
    - **A variable must be declared with a datatype before its use.**
    - **It must be initialized with an *initializer* before use**.


3. **Definition: Statically Typed Language is a Programming Language in which the Programmer needs to specify the type of data a variable can hold *EXPLICITLY* so that the Compiler can detect the common type errors long before the program actually executes**.

---
### **Question: Do you think that Java is still statically typed after the introduction of Local Variable Type Inferencing in JDK 10.?**
---

## **Fooling around with Java Datatypes**.

1. [**View the Type Dissociation into Primitive and Non-Primitive**](https://s4.aconvert.com/convert/p3r68-cdx67/ae6mw-m0yl6.svg)

2. In the image shown above, it is clear that there are two forms of Datatypes namely: **Primitive and Non-Primitive**.


#### ***Primitive Datatypes***
* **Signed Numbers --> Signed Numbers are numbers whose range is from a negative to a positive number and these numbers contain the Most Significant Bit which denotes whether the number is negative or positive.**
* **Datatypes having a fixed range and a predefined size built for just improving the efficiency of the program that cannot be instantiated, are called Primitive Datatypes.**
* But what is **Instantiation**?
* **Instantiation means creating the objects so that its properties(variables) like hair color, skin color, etc. and behavior(methods) like eating, sleeping, etc. can be accessed.** We will learn more about Instantiation in the subsequent notes of Object Oriented Programming.
* There are some **special characteristics** of these types: -
    - **They have a fixed size.** 
    Eg: [**Visit this Link**](https://www.middleschoolchemistry.com/img/content/lessons/3.2/girl_examining_cylinder_in_graduated_cylinder.jpg) You have measuring cylinders which consumes some area when placed on a table.
    - **They have a fixed range.**
    Eg: For a measuring cylinder, they can store only a fixed volume. If we try to fill more, an overflow happens. In Java, overflow of range in case of Primitive types results in a syntax error namely **integer number too large**.
    - **They store a specific datatype**
        Eg: You store water in an overhead tank and not fruit juice. In case of Java, if there is a type mismatch, then a syntax error namely **incompatible types**.
    - **You cannot create the object of Primitive types**
    EG:
    ``` Java
        int a = new int(20);        //Results in an error.
        int a = 20;         //Works Successfully
    
    ```
* Its important to see the division of Java Datatypes in the Primitive and Non-Primitive Hierarchy. If you not yet seen it, its important to see it...

##### **Why there are Primitive types at all in Java?**
1. Answer to this, it is just for increasing the efficiency of a Java Program both by Memory and Time. 
2. As already mentioned, its easier for you to choose a vessel prior to filling up the liquid in the vessel. 
3. Now watch this dramatic conversation between a Compiler and a Programmer on the program given below.
 ``` Java
     public class Demo3{
         public static void main(String args[]){
             int a = 20;
             double b = 90.4543;
             char ch = 'a';
        }
    }
 ```
 **Programmer**: Hey *Compiler*, please **compile** this source code and create a bytecode file.
 **Compiler**: Okay dude, there are no syntax errors and everything seems fine. I am compiling the code...Please wait a moment.
 **Compiler**: Hey Pal, I have compiled the code and have mentioned **how many bytes of memory should be allocated for the Primitive types you initialized in the ByteCode**.(*Bytecode or intermediate code is the highly optimized, platform independent set of instructions that is passed to the JVM to be converted to Machine Native Code.*)
 **Programmer**: Why do you need to tell the JVM that how much size is to be required?
 **Compiler**: It is necessary Pal. If I dont inform JVM about the size, it would have to search it by himself and that would take a lot of time.
 **Compiler**: Moreover, I cannot let you and JVM struggle for time and space.
 **Programmer**: Greatful to you, my friend.


4. So, this is the dramatic reason why Primitive types have a fixed range and size.

---
Time to know about the Primitive Datatypes one by one.
# **Integral Datatypes**
## **byte**
1. **Size --> 1 Byte or 8 bits.**
2. **Range --> -128 to 127.**
3. Generally used in case of **transferring Strings across Networks and writing files with Character and Byte Streams**.
4. **MAX_VALUE :  127**
5. **MIN_VALUE : -128**
6. ![](https://i.imgur.com/C2lfz1T.jpg)
7. The **MSD** stands for **Most Significant Bit**. This stores either 0(negative) or 1(positive). **In Signed Integers, this MSD signifies whether the number stored is positive(zero or more than zero) or negative(less than zero).**
8. If you add **2^6 + 2^5 + 2^4 + 2^3 + 2^2 + 2^1 + 2^0**, you would get the sum as **127**.
 
### **Operations on a *byte* datatype**
1. ``` Java
        public class Demo4{
            public static void main(String[] args){
                double a = 20.52;
                byte b = a; //Possible Loss of Precision.
            }
        }
   ```
2. ``` Java
    
        public class Demo5{
            public static void main(String[] args){
                String str = "Krish Jaiswal";
                byte b = str;    // Incompatible Types. found: java.lang.String ; required: byte
            }
        }

    ```
   **Infamous Error in case of Datatypes are :-**
   1. **Possible Loss of Precision**: It is caused due ***to possible loss of some value during assignment to a variable having a different type***.
   2. **Incompatible Types**: It is caused when two datatypes, which are ***not compatible and hold no relation with each other are assigned or explicitly casted.***
---
## **short**
1. **Size --> 2 Byte or 16 bits.**
2. **Range --> -32768 to 32767.**
3. Was **previously used for Intel 8086 16 bit Processors which existed during late 1990s and early 2000s since it provided efficiency there too.**
4. **MAX_VALUE :  32767**
5. **MIN_VALUE : -32768**
6. The **MSD** stands for **Most Significant Bit**. This stores either 0(negative) or 1(positive). **In Signed Integers, this MSD signifies whether the number stored is positive(zero or more than zero) or negative(less than zero).**
8. If you add **2^15 + 2^14 + 2^13 + 2^12 + 2^11 + 2^10 + 2^9** + ..., you would get the sum as **32767**.
 
### **Operations on a *short* datatype**
1. ``` Java
        public class Demo6{
            public static void main(String[] args){
                double a = 20.52;
                short b = a; //Possible Loss of Precision.
            }
        }
   ```
2. ``` Java
    
        public class Demo7{
            public static void main(String[] args){
                String str = "Krish Jaiswal";
                short b = str;    // Incompatible Types. found: java.lang.String ; required: short
            }
        }

    ```
---
## **int**
1. **Size --> 4 Bytes or 32 bits.**
2. **Range --> -2147483648 to 2147483647.**
3. It is the **default integral datatype. It is frequently used. It has a wide range of uses.**
4. **MAX_VALUE :  2147483647**
5. **MIN_VALUE : -2147483648**
6. If you add **2^31 + 2^30 + 2^29 + 2^28 + 2^27 + 2^26 + 2^25** + ..., you would get the sum as **2147483647**.
 
### **Operations on a *int* datatype**
1. ``` Java
        public class Demo8{
            public static void main(String[] args){
                int b = 10l; //Possible Loss of Precision since "l" denotes a long datatype.
            }
        }
   ```
2. ``` Java
    
        public class Demo9{
            public static void main(String[] args){
                String str = "Krish Jaiswal";
                int b = str;    // Incompatible Types. found: java.lang.String ; required: int
            }
        }

    ```
3. ``` Java
    
        public class Demo10{
            public static void main(String[] args){
                int a = 20;
                int b = a*4+1;
                System.out.println(b);
            }
        }

    ```

## **long**
1. **Size --> 8 Bytes or 64 bits.**
2. **Range --> -9_223_372_036_854_775_808 to 9_223_372_036_854_775_807.**
3. It is a signed 64 bit type used for storing excessive large or small numbers that may surpass the range of **int** datatype.
4. **MAX_VALUE :  9_223_372_036_854_775_807**
5. **MIN_VALUE : -9_223_372_036_854_775_808**
6. If you add **2^63 + 2^62 + 2^61 + 2^60 + 2^59 + 2^58 + 2^57** + ..., you would get the sum as **9_223_372_036_854_775_807**.

### **Operations on *long* datatype.**

1. ``` Java
    
        public class Demo11{
            public static void main(String[] args){
                String str = "Krish Jaiswal";
                long b = str;    // Incompatible Types. found: java.lang.String ; required: int
            }
        }

    ```
2. ``` Java
        public class Demo12{
            public static void main(String[] args){
                long var1 = 104 * 203 ;
                long var2 = 2147483648 ; //Gives a compile time error: integer number too large.
                /*
                * A long datatype has a default value as 0l. 
                * Here 'l' denotes that the number is of long type. 
                * Since all numbers are by default of 'int' type, Compiler gives an error if it finds that the range is exceeded.
                */
                
                long var3 = 2147483648l ; // No Error.
            }
        }
    ```
---
# **Floating-Point Types**

1. Java implements the standards of IEEE 754 set of floating point types and operators.
2. Floating Point means **real numbers**. 
    Eg: There are 2 consecutive numbers. Let's say 20 and 21. So the number between 20 and 21 can be 20.302, 20.1, 20.2, etc. 
    
## **float**
1. **Size --> 4 Bytes or 32 bits.**
2. **Range --> 1.4e-045 to 3.4e+38.**
3. It specifies a *single-precision* value that uses 32 bits of storage. Single precision are useful on some processors and hence is used in storing floating point values.

### **Operations on *float* datatype**
1. ``` Java
        public class Demo13{
            public static void main(String[] args){
                float f = 2.13421f;
                /*
                * Since all the floating point numbers have 'double' type as default type, we need to explicitly specify that our number is a float type.
                * This is done by adding 'f' to the number.               
                */
                
                float f2 = 32.3212123 ; //Compile Time Error occurs: Possible Loss of Precision.
            }
        }
    ```

## **double**
1. **Size --> 8 Bytes or 64 bits.**
2. **Range --> 4.9e-324 to 1.8e+308 .**
3. It specifies a Double Precision that uses 64 bit of storage. It is the default datatype for all floating datatypes.

###  **Operations on *double* datatype**
1. ``` Java
        public class Demo14{
            public static void main(String[] args){
                double d = 2.48213121;
            }
        }
    ```

---
# **Character**

## **char**
1. This datatype is **used to store characters.** 
2. It uses **Unicode standard that is a fully international character set of 2^16 characters containing Arabic, Chinese, Hebrew, etc. totalling to 65,535 characters.**
3. It is **not a signed datatype. It means that it cannot have a negative value**.
4. Unicode system is combination of other smaller character sets like **ISO-Latin1** and **ASCII.**
5. Characters are **internally represented as integral numbers.**
Eg: Try executing this code:-
    ``` Java
        public class Demo15{
            public static void main(String[] args){
                char ch = 'a';
                int asc = ch;    //Compiler internally represents a character as an integer number and hence assigning a character to an integer type variable gives no errors at all.
                System.out.println("Integer Value of "+ch+" is : "+asc);
            }
        }
    ```
    Output: - 
    ```
        Integer Value of a is : 97
    ```
6. We would be understanding **Implicit Type Casting** in some other lectures.

# **Boolean**

## **boolean**
1. Does your toothpaste have salt in it?
2. Are you 54 years old?
3. *boolean* is a datatype which helps us to **classify a condition in ***true*** and ***false***** .
4. So, imagine this situation:-
    - Person 1: Is it sunny Outside?
    - Person 2: No (false).
    - Person 2: Should we carry umbrella?
    - Person 1: No (false).
5. These things are represented by **boolean** datatype.
6. All **Relational and Logical conditions are either in true or in false, which means they have **boolean** as the only type.**
7. Interestingly, it **cannot be type casted (either implicitly or explicitly) to any other datatype.** Doing that would give a Compile Time Error : **incompatible types**.

### **Operations on *boolean* datatype**
1. ``` Java
        public class Demo16{
            public static void main(String[] args){
                boolean b = true;
                boolean x = false;
                
                int a = 20;
                boolean result = (a>20)?true:false;    //Ternary Operations would be covered in subsequent lectures.
                int val = 1;
                boolean wrong = val; //Compile Time Error. Incompatible types.
            }
        }
    ```
---
# **How Prepared you Are?**
1. What would be the first line to generate an error in this program.: -
    ``` Java
        public class Test2{
            public static void main(String[] args){
                int a = 10.34;         // 1
                double b = 45.302f;    //2
                char ch = 97;        //3;
            }
        }
    ```
2. Why Java makes use of primitive datatypes?
3. Predict the Output:-
    ``` Java
        public class Test3{
            public static void main(String[] args){
                int g = 'a';
                System.out.println(g);
            }
        }
    ```
4. Predict the Output: -
    ``` Java
        public class Test4{
            public static void main(String[] args){
                double 2ft = 50.32f;   
            }
        }
    ```
---
# **Variables**
1. **Definition: Variables are just like vessels which store some specific thing. In tech terms, Variables are *user-allocated memory locations* which store some value and their value can be changed during the execution of a program**.
2. **user-allocated** since user tells the compiler to reserve the memory location for a vessel of *x* type.
3. All variables are identifiers so they follow all the naming conventions of identifiers.

## **Identifier VS Variable**


| Identifier | Variable 
| -------- | -------- | 
| Identifier is a unique name given to each and every entity of a program for its unique identification in the whole program.| Variables are user allocated memory locations that hold some value which can be   changed during the execution of the program.|
| They are used for identification purposes. | They are used for storing values of a given type|

---
# **Frequently Asked Questions**
## ***Even when char and short have the same size, they have different range.***
Answer: *char* is not a integer or floating point datatype. It means that it cannot have any negative value. Hence the Most Significant Bit would be free since it need not store any 0 or 1 for denoting a positive or negative number.But *short* is a integral datatype used for storing integers. So, the Compiler should be made aware that the number stored in a variable of type *short* is positive or negative. Hence the Most Significant Bit stores 0 or 1 denoting the number as positive or negative.  Hence, **char being of 2 bytes has a max range of 65,535 and short being of 2 bytes has a max range of 32767**

---

## ***Why using float is not preferred when dealing with higher floating point values.***
Answer: *float* results in loss of precision at higher values. Hence it is not safe to use float with higher floating point values.

