# Lab 2: David Carboch

### 2-bit comparator

1. Karnaugh maps for other two functions:

   Greater than:

   ![K-map_GT](https://user-images.githubusercontent.com/99664755/155090766-f4cc5c15-b572-4b14-a5f9-37135a32d3df.png)


   Less than:

   ![K-map_LT](https://user-images.githubusercontent.com/99664755/155091580-02cc8a71-695b-4364-b714-88593482c75b.png)


2. Equations of simplified SoP (Sum of the Products) form of the "greater than" function and simplified PoS (Product of the Sums) form of the "less than" function.

   ![Logic functions](https://user-images.githubusercontent.com/99664755/155093084-ef733be9-cce5-46f4-8a17-f5edaafcd6dc.png)


### 4-bit comparator

1. Listing of VHDL stimulus process from testbench file (`testbench.vhd`) with at least one assert (use BCD codes of your student ID digits as input combinations). Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

   Last two digits of my student ID: **xxxx54??**

```vhdl
    p_stimulus : process
    begin
        -- Report a note at the beginning of stimulus process
        report "Stimulus process started" severity note;

        -- First test case
        s_b <= "0101";        -- Such as "0101" if ID = xxxx54
        s_a <= "0100";        -- Such as "0100" if ID = xxxx54
        wait for 100 ns;
        -- Expected output
        assert ((s_B_greater_A = '1') and
                (s_B_equals_A  = '0') and
                (s_B_less_A    = '0'))
        -- If false, then report an error
        report "Input combination COMPLETE_THIS_TEXT FAILED" severity error;

        -- Report a note at the end of stimulus process
        report "Stimulus process finished" severity note;
        wait;
    end process p_stimulus;
```

2. Text console screenshot during your simulation, including reports.

   ![Console screenshot](https://user-images.githubusercontent.com/99664755/155100169-932444f3-9726-4498-8ff5-ebac752344d6.png)


3. Link to your public EDA Playground example:

   [https://www.edaplayground.com/...](https://www.edaplayground.com/...)
   
   [4-bit comaparator edaplayground](https://www.edaplayground.com/x/iVAR)
