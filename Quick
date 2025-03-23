import java.util.Random;
import java.util.Scanner;
public class Quick{
    static int count = 0;
    static int partition(int a[], int l, int r) {
        int pivot = a[r];
        int temp;
        int i = l - 1;
        for (int j = l; j < r; j++) {
            count++;
            if (a[j] < pivot) {
                i++;
                temp = a[i];
                a[i] = a[j];
                a[j] = temp;
            }
        }
        temp = a[i + 1];
        a[i + 1] = a[r];
        a[r] = temp;
        return i + 1;
    }
    static void quicksort(int a[], int l, int r) {
        if (l < r) {
            int s = partition(a, l, r);
            quicksort(a, l, s - 1);
            quicksort(a, s + 1, r);
        }
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the number of elements:");
        int n = sc.nextInt();
        int[] a = new int[n];
        Random rand = new Random();
        System.out.println("Input array (random numbers):");
        for (int i = 0; i < n; i++) {
            a[i] = rand.nextInt(1000);
            System.out.print(a[i] + " ");
        }
        System.out.println();
        quicksort(a, 0, n - 1);
        System.out.println("Sorted numbers:");
        for (int i = 0; i < n; i++) {
            System.out.print(a[i] + " ");
        }
        System.out.println();
        System.out.println("Best case: " + (int) (n * Math.log(n) / Math.log(2)));
        System.out.println("Number of basic operations: " + count);
        System.out.println("Worst case: " + (n * n));
    }
}
