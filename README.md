public class PatternProgram {
    public static void main(String[] args) {
        int n = 7; // The size of the grid (7x7)
        int maxVal = 4; // The starting outer number

        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= n; j++) {
                
                // Calculate distance to the four edges
                int top = i;
                int bottom = n - i + 1;
                int left = j;
                int right = n - j + 1;

                // The 'layer' is the minimum distance to any edge
                int minDistance = Math.min(Math.min(top, bottom), Math.min(left, right));

                // Print the value: maxVal - minDistance + 1
                System.out.print((maxVal - minDistance + 1) + " ");
            }
            // Move to the next line after each row
            System.out.println();
        }
    }
}
