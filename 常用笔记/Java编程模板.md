# 从map拿取一个值并做NULL校验

```java
map.getOrDefault("key", "defaultValue");
Optional.ofNullable(map.get("key")).orElse("defaultValue");
```



# 钩子方法实现

```java
public abstract class AbstractClass
{
    /**
    *返回boolean的抽象方法，由子类实现
    */
    public abstract boolean isTrue();
    
    /**
    *父类方法，可自由决定是否可被重写
    */
    public final void execute()
    {
        if(isTrue())
        {
            //do something
        }
    }  
}

public class SubClass extends AbstractClass
{
    public abstract boolean isTrue()
    {
        return true;
    }
    public static void main(String[] args)
    {
        SubClass test = new SubClass();
        test.execute();
    }
}

```

