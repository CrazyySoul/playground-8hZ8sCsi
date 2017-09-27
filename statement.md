There are multiple ways to iterate or loop a Map in Java.

## Using foreach in Java 8

```java runnable
// { autofold
import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;

public class Main {

public static void main(String[] args) {
// }

    Map<Integer, String> customers = new HashMap<>();
		customers.put(1, "Jhon");
		customers.put(2, "Smith");
		customers.put(3, "Sally");

		customers.forEach((id, name) -> {
			System.out.println("Key : " + id + " value : " + name);
		});

//{ autofold
}

}
//}
```

## Using stream() in Java 8

```java runnable
// { autofold
import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;

public class Main {

public static void main(String[] args) {
// }

    Map<Integer, String> customers = new HashMap<>();
		customers.put(1, "Jhon");
		customers.put(2, "Smith");
		customers.put(3, "Sally");

		System.out.println("");
		customers.entrySet().stream().forEach(e ->
				System.out.println("Key : " + e.getKey() + " value : " + e.getValue())
		);

//{ autofold
}

}
//}
```

## Using entrySet()

```java runnable
// { autofold
import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;

public class Main {

public static void main(String[] args) {
// }

    Map<Integer, String> customers = new HashMap<>();
		customers.put(1, "Jhon");
		customers.put(2, "Smith");
		customers.put(3, "Sally");

    for (Map.Entry<Integer, String> entry : customers.entrySet()) {
      System.out.println("Key : " + entry.getKey() + " value : " + entry.getValue());
    }

//{ autofold
}

}
//}
```

## Using keySet()

```java runnable
// { autofold
import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;

public class Main {

public static void main(String[] args) {
// }

    Map<Integer, String> customers = new HashMap<>();
		customers.put(1, "Jhon");
		customers.put(2, "Smith");
		customers.put(3, "Sally");

    for (Integer key : customers.keySet()) {
      System.out.println("Key : " + key + " value : " + customers.get(key));
    }
//{ autofold
}

}
//}
```

## Using iterator through map

```java runnable
// { autofold
import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;

public class Main {

public static void main(String[] args) {
// }

    Map<Integer, String> customers = new HashMap<>();
		customers.put(1, "Jhon");
		customers.put(2, "Smith");
		customers.put(3, "Sally");

		Iterator<Map.Entry<Integer, String>> iterator = customers.entrySet().iterator();
		while (iterator.hasNext()) {
			Map.Entry entry = iterator.next();
			System.out.println("Key : " + entry.getKey() + " value : " + entry.getValue());
		}
//{ autofold
}

}
//}
```

## Using iterator through the KeySe

```java runnable
// { autofold
import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;

public class Main {

public static void main(String[] args) {
// }

    Map<Integer, String> customers = new HashMap<>();
		customers.put(1, "Jhon");
		customers.put(2, "Smith");
		customers.put(3, "Sally");

		Iterator<Integer> iterator = customers.keySet().iterator();
		while (iterator.hasNext()) {
			Integer key = iterator.next();
			System.out.println("Key : " + key + " value : " + customers.get(key));
		}
//{ autofold
}

}
//}
```

Original post :- http://mydevgeek.com/6-ways-iterate-loop-map-java/
