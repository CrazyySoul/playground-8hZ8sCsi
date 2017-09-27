There are multiple ways to iterate or loop a Map in Java.

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

		System.out.println("Using foreach in Java 8");
		customers.forEach((id, name) -> {
			System.out.println("Key : " + id + " value : " + name);
		});
    System.out.println("------------------------");

		System.out.println("Using stream() in Java 8");
		customers.entrySet().stream().forEach(e ->
				System.out.println("Key : " + e.getKey() + " value : " + e.getValue())
		);
    System.out.println("------------------------");

		System.out.println("Using entrySet()");
		for (Map.Entry<Integer, String> entry : customers.entrySet()) {
			System.out.println("Key : " + entry.getKey() + " value : " + entry.getValue());
		}
    System.out.println("------------------------");

		System.out.println("Using keySet()");
		for (Integer key : customers.keySet()) {
			System.out.println("Key : " + key + " value : " + customers.get(key));
		}
    System.out.println("------------------------");

		System.out.println("Using iterator through map");
		Iterator<Map.Entry<Integer, String>> iterator = customers.entrySet().iterator();
		while (iterator.hasNext()) {
			Map.Entry entry = iterator.next();
			System.out.println("Key : " + entry.getKey() + " value : " + entry.getValue());
		}
    System.out.println("------------------------");

		System.out.println("Using iterator through the KeySet");
		Iterator<Integer> iterator1 = customers.keySet().iterator();
		while (iterator1.hasNext()) {
			Integer key = iterator1.next();
			System.out.println("Key : " + key + " value : " + customers.get(key));
		}
    System.out.println("------------------------");

//{ autofold
}

}
//}
```

Original post :- http://mydevgeek.com/6-ways-iterate-loop-map-java/
