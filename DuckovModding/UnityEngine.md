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
