# ArrayEx
package array;

import java.util.ArrayList;
import java.util.Collection;
import java.util.HashMap;
import java.util.Set;

/* a3.(頻度統計,histogram) 亂數產生1000個介於1~10的整數,
 *    請統計1~10各出現多少次.*/

public class Histogram {
	
	public static void main(String[] args) {
		int i = 0;
		ArrayList<Integer> array = new ArrayList<>();
		HashMap<Integer, Integer> map = new HashMap<>();
		while (i < 5) {
			int random = (int)(10*Math.random());
			if (random != 0) {
				array.add(random);
			} else {
				continue;
			}
			i++;
		}
		System.out.println(array);
		
		for (Integer num : array) {
			Integer count = map.getOrDefault(num, 0);
			if (!map.containsKey(num)) {
				count++;
				map.put(num, count);
			} else {
				count++;
				map.put(num, count);
			}
		}
		System.out.println(map);
		
		Set<Integer> keys = map.keySet();
		Collection<Integer> values = map.values();
		System.out.println(keys);
		System.out.println(values);

	}

}
