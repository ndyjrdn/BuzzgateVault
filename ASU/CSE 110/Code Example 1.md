
    ```
    class Main {
  public static void main(String[] args) {
    int[][] populations = 
    {
        { 106, 107, 111, 133,  221,  767, 1766 },
        { 502, 635, 809, 947, 1402, 3634, 5268 }, 
        {   2,   2,   2,   6,   13,   30,   46 }, 
        { 163, 203, 276, 408,  547,  729,  628 }, 
        {   2,   7,  26,  82,  172,  307,  392 }, 
        {  16,  24,  38,  74,  167,  511,  809 }
    };

    String[] continents = 
    { 
        "Africa", 
        "Asia", 
        "Australia",
        "Europe", 
        "North America", 
        "South America" 
    };

    printTable(populations, continents);
  }
  ################################################
  Main is above this.  declares and instantiates the variables.  
  methods are created below
####################################################
  static void printTable(int[][] populations, String[] continents) {
    System.out.println("       CONTINENT |   1750  1800  1850  1900  1950  2000  2050");
    System.out.println("-----------------+-------------------------------------------");
    printTableBody(continents, populations);
    System.out.println("-----------------+-------------------------------------------");
    System.out.print  ("          TOTALS : ");
    printColumnTotals(populations);
  }
##########################################################
loop over 1 and 2 d arrays.
#########################################################
  static void printTableBody(String[] continents, int[][] populations) {
    for (int row = 0; row < populations.length; row++) {
      System.out.printf("%16s | ", continents[row]);
      printRowData(populations, row);
    }
  }
##########################################################
loop over 2 d arrays.
#########################################################
  static void printRowData(int[][] populations, int row) {
    for (int col = 0; col < populations[row].length; col++) {
        int population = populations[row][col];
        System.out.printf("%6d", population);
      }
      System.out.println();
  }
##########################################################
loop over 2 d array and calculate column totals.
#########################################################
  static void printColumnTotals(int[][] populations) {
    for (int col = 0; col < populations[0].length; col++) {
      int total = 0;
      for (int row = 0; row < populations.length; row++) {
        total += populations[row][col];
      }
      System.out.printf("%6d", total);
    }
  }
}
    ```