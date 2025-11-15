# Coroutine

## Base method

```C#
using System.Collections;

namespace BlahBlahBlah {

    public static class Anything {

        public static void IEnumarator SthRoutine() {
            while(true){
                doSomething();
                yield return new WaitForSeconds(<float>time);
            }
        } 
    }
}
```

## To Use

```C#
using UnityEngine;

namespace BlahBlahBlah {
    
    // Which Inherit Mono
    public class SomeWhereElse:MonoBehaviour {


        void WhenToStart() {

            // Mono's method
            StartCourtine(Anything.SthRoutine());
        }

        void WhenToEnd() {

            // Mono's method
            StopCourtine(Anything.SthRoutine());
        }
    }
}
```

## Why This?

I should have used this a long time ago… Why bother using time? This one can directly run based on conditions, and you can set when it starts and ends. Isn’t that great?
