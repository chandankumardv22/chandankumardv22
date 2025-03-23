import java.util.Scanner;0
public class topsorts {
    static int n;
    static int[][] cost = new int[10][10];
    static int[] indegree = new int[10];
    static boolean[] removed = new boolean[10];
    static void calculate() 
    {
        for (int i = 0; i < n; i++) 
            indegree[i] = 0;
        for (int i = 0; i < n; i++)
            for (int j = 0; j < n; j++)
                if (cost[i][j] == 1) 
                  indegree[j]++;
    }
    static void sourceRemoval() {
        System.out.println("Topological Order:");
        for (int count = 0; count < n; count++) {
            calculate();
            int source = -1;
            for (int i = 0; i < n; i++)
                if (!removed[i] && indegree[i] == 0) {
                    source = i;
                    break;
                }
            if (source == -1) {
                System.out.println("Graph is cyclic, no solution.");
                return;
            }
            System.out.print(source + " ");
            removed[source] = true;
            for (int k = 0; k < n; k++) cost[source][k] = 0;
        }
        System.out.println();
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter number of vertices: ");
        n = sc.nextInt();
        System.out.println("Enter adjacency matrix:");
        for (int i = 0; i < n; i++)
            for (int j = 0; j < n; j++)
                cost[i][j] = sc.nextInt();
        sourceRemoval();
    }
}
