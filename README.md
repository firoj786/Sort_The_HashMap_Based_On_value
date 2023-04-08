# Sortthe_HashMap_BasedOnvalue

package com.nt.solve.code;

import java.util.HashMap;

import java.util.LinkedHashMap;

import java.util.Map;

import java.util.stream.Collectors;

/**
 * @author Firoj
 * @since 2022-01-05
 */
public class SorttheHashMapBasedOnvalue {

	public static void main(String[] args) {
	
		Map<String, Integer> map = new HashMap<>();
		
		map.put("firoj", 2);
		
		map.put("husne", 4);
		
		map.put("arzoo", 5);
		
		map.put("dipu", 3);
		
		map.put("tanish", 6);
		
		map.put("ibney", 1);

		System.out.println("Befor Sorting:-" + map);
		LinkedHashMap<String, Integer> sortedMap = map.entrySet().stream().sorted((e1, e2) -> {
			return e1.getValue() - e2.getValue();
		}).collect(Collectors.toMap(Map.Entry::getKey, Map.Entry::getValue, (e1, e2) -> e1, LinkedHashMap::new));
		System.out.println("After sorting :- " + sortedMap);
	}
}
