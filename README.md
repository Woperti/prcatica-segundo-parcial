# Remover el elemento


```Java
class Solution {
    public int removeElement(int[] nums, int val) {
       
    }
}
```

Problema: 

Crear en Java una clase con un constructor
1. Crear un diagrama de flujo que de la solucion.
2. Implementar una solucion para estos casos: 

Funcion de testing
```Java
public class TestSolution {
    public static void main(String[] args) {
        Solution solution = new Solution();
        
        int[] nums1 = {3, 2, 2, 3};
        int val1 = 3;
        testRemoveElement(solution, nums1, val1, 2, new int[]{2, 2});
        
        int[] nums2 = {0, 1, 2, 2, 3, 0, 4, 2};
        int val2 = 5;
        testRemoveElement(solution, nums2, val2, 8, new int[]{0, 1, 2, 2, 3, 0, 4, 2});
        
        int[] nums3 = {1, 1, 1, 1};
        int val3 = 1;
        testRemoveElement(solution, nums3, val3, 0, new int[]{});
        
        // Caso de prueba 4: Ninguno de los elementos es el valor a remover
        int[] nums4 = {2, 3, 4, 5};
        int val4 = 1;
        testRemoveElement(solution, nums4, val4, 4, new int[]{2, 3, 4, 5});
        
        int[] nums5 = {};
        int val5 = 1;
        testRemoveElement(solution, nums5, val5, 0, new int[]{});
    }

    private static void testRemoveElement(Solution solution, int[] nums, int val, int expectedLength, int[] expectedNums) {
        int resultLength = solution.removeElement(nums, val);
        System.out.println("Expected Length: " + expectedLength + ", Result Length: " + resultLength);
        
        // Verificar si el tamaño coincide
        if (resultLength != expectedLength) {
            System.out.println("Test failed! Expected length does not match.");
            return;
        }
        
        for (int i = 0; i < resultLength; i++) {
            if (nums[i] != expectedNums[i]) {
                System.out.println("Test failed! Element mismatch at index " + i);
                return;
            }
        }
        System.out.println("Test passed!");
    }
}
```
