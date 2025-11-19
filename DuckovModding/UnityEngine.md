# UnityEngine

## Notes

###

Instantiating a class directly using new is ineffective — you need to create a GameObject first, then attach the desired class to it using AddComponent\<Class\>() for it to function properly within the engine.

### Cool Stuff

```C#
namespace MyDll

public class MyClass
{

    [DllImport("kernel32.dll")]
    static extern bool AllocConsole();

    [DllImport("kernel32.dll")]
    static extern IntPtr GetStdhandle(int nStdHandle);

    [DllImport("kernel32.dll")]
    static extern bool SetConsolemode(IntPtr hConsoleHandle, int mode);

    public static void InitWithConsole()
    {
    AllocConsole();
    Console.SetOut(new StreamWriter(Console.OpenStandardOutput())
    {
        AutoFlush = true
    });
    Console.WriteLine("Console Ready");
    }

}
```

### Reflections

I spent half a day—half a day!—just to get thermal imaging working! Reflection in C# feels a lot like casting in Unreal Engine. At its core, it allows the program to access an object at runtime through various means, and once it's correctly cast, you can inspect its properties, modify its contents, and invoke its methods.
The most crucial step is that moment when you reach into the mirror to grasp a part of yourself—you need to be clear about which part you're reaching for, what state it's in, and what type it is.
