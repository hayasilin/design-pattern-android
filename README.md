# Android Design Pattern

This is review of this book: [Design Pattern Android](https://www.tenlong.com.tw/products/9789864340941?list_name=srh).

This book demonstrates design pattern that is used in Android.

I pick up some important contents from each chapter and sample code from the book. Enjoy it.

## Table of Contents
- [Chapter 2 Singleton pattern](#chapter-2-singleton-pattern)
- [Chapter 3 Builder pattern](#chapter-3-Builder-pattern)
- [Chapter 4 Prototype pattern](#chapter-4-prototype-pattern)
- [Chapter 5 Factory method pattern](#chapter-5-factory-method-pattern)
- [Chapter 6 Abstract factory pattern](#chapter-6-abstract-factory-pattern)
- [Chapter 7 Strategy pattern](#chapter-7-strategy-pattern)
- [Chapter 8 State pattern](#chapter-8-state-pattern)
- [Chapter 9 Chain of responsibility pattern](#chapter-9-chain-of-responsibility-pattern)
- [Chapter 10 Interpreter pattern](#chapter-10-interpreter-pattern)
- [Chapter 11 Command pattern](#chapter-11-command-pattern)
- [Chapter 12 Observer pattern](#chapter-12-observer-pattern)
- [Chapter 13 memo pattern](#chapter-13-memo-pattern)
- [Chapter 14 Iterator pattern](#chapter-14-iterator-pattern)
- [Chapter 15 Template pattern](#chapter-15-template-pattern)
- [Chapter 16 Visitor pattern](#chapter-16-visitor-pattern)
- [Chapter 17 Mediator pattern](#chapter-17-mediator-pattern)
- [Chapter 18 Proxy pattern](#chapter-18-proxy-pattern)
- [Chapter 19 Composite pattern](#chapter-19-composite-pattern)
- [Chapter 20 Adapter pattern](#chapter-20-adapter-pattern)

## Chapter 2 Singleton pattern

**Android source code that use this design pattern:**

- LayoutInflater
- Context

## Chapter 3 Builder pattern

**Android source code that use this design pattern:**

- AlertDialog.Builder

## Chapter 4 Prototype pattern

**Android source code that use this design pattern:**

- ArrayList.clone()
- Intent

```java
Intent shareIntent = new Intent(Intent.ACTION_SENDTO, uri);
shareIntent.putExtra("sms_body", "The SMS text");
Intent intent = (Intent) shareIntent.clone();
startActivity(intent);
```

## Chapter 5 Factory method pattern

**Android source code that use this design pattern:**

- ArrayList and HashSet ’s iterator function use factory method pattern
- onCreate

## Chapter 6 Abstract factory pattern

**Android source code that use this design pattern:**

- onCreate
- onBind
- MediaPlayer: MediaPlayerFactory, StagefrightPlayerFactory

## Chapter 7 Strategy pattern

**Android source code that use this design pattern:**

- TimeInterpolator used for animation: LinearInterpolator, AccelerateDecelerateInterpolator, DecelerateInterpolator

## Chapter 8 State pattern

**Android source code that use this design pattern:**

- Wifi state

## Chapter 9 Chain of responsibility pattern

**Android source code that use this design pattern:**

- BroadcastReceiver, normal broadcast, ordered broadcast

## Chapter 10 Interpreter pattern

**Android source code that use this design pattern:**

- AndroidManifest.xml, PackageParser to get the set up from AndroidManifest,xml

## Chapter 11 Command pattern

**Android source code that use this design pattern:**

- NotifyArgs - interface, NotifyKeyArgs - concrete class, InputDispatcher - receiver
- PackageManagerService
  - HandlerParams - abstract
    - InstallParams - concrete
    - MoveParams - concrete
    - MeasureParams - concrete

## Chapter 12 Observer pattern

**Android source code that use this design pattern:**

- ListView’s setAdapter ’s notifyDataSetChanged
- BroadcastReceiver

## Chapter 13 memo pattern

**Android source code that use this design pattern:**

- Activity
  - onSaveInstanceState
  - onRestoreInstanceState

## Chapter 14 Iterator pattern

**Android source code that use this design pattern:**

- List, Map’s iterator
- SQLiteDatabase’s query will return a Cursor, which is a iterator of the query result

## Chapter 15 Template pattern

**Android source code that use this design pattern:**

- AsyncTask
  - Execute -> onPreExecute -> doInBackground -> onPostExecute

- Activity
  - onCreate -> onStart -> onResume

## Chapter 16 Visitor pattern

This is the most complicate pattern among the all patterns.
According to GOF’s author interview, usually you don’t need to use visitor patter. If you do that means you really need it.

**Android source code that use this design pattern:**

- Annotation
- Interface Element’s accept is a typical visitor pattern

## Chapter 17 Mediator pattern

**Android source code that use this design pattern:**

- KeyguardViewMediator

## Chapter 18 Proxy pattern

**Android source code that use this design pattern:**

- ActivityManagerProxy
- ActivityManagerNative’s ActivityManagerService

## Chapter 19 Composite pattern

**Android source code that use this design pattern:**

- View and ViewGroup’s nest structure

## Chapter 20 Adapter pattern

**Android source code that use this design pattern:**

- ListView’s adapter

- RecycleView