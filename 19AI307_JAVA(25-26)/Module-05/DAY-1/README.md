# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write text into a file using FileOutputStream.

## AIM:
To write a Java program using FileOutputStream to write text data into a file.

## ALGORITHM :
```
1.Start the program.
2.Import the necessary package 'java.util'
3.Create a FileOutputStream object with a file name (e.g., "output.txt").
4.Store a text message in a string.
5.Convert the string into a byte array using getBytes().
6.Use write() method of FileOutputStream to write the bytes into the file.
7.Close the stream using the close() method.
8.If an exception occurs, handle it using try-catch.
9.End the program.
```




## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Agalya R
RegisterNumber: 212222040003
*/
```

## SOURCE CODE:
```
import java.io.FileWriter;
import java.io.IOException;
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        try{
            String str=sc.next();
            String content=sc.next();
            FileWriter f=new FileWriter(str);
            f.write(content);
            System.out.print("File written successfully.");
        }
        catch(IOException e)
        {
            System.out.println("Error occured");
        }
    }
}

```







## OUTPUT:

<img width="1215" height="418" alt="image" src="https://github.com/user-attachments/assets/8030601f-ffbd-4c54-b242-0882eb8b8401" />



## RESULT:
The program successfully writes text into a file using FileOutputStream by converting text into bytes and storing it in a newly created file named output.txt.

