# ssc1.1library IEEE;
use IEEE.STD_LOGIC_1164.ALL;
use IEEE.STD_LOGIC_UNSIGNED.ALL;
-- Uncomment the following library declaration if using
-- arithmetic functions with Signed or Unsigned values
--use IEEE.NUMERIC_STD.ALL;

-- Uncomment the following library declaration if instantiating
-- any Xilinx leaf cells in this code.
--library UNISIM;
--use UNISIM.VComponents.all;

entity num4Sim is

end num4Sim;

architecture Behavioral of num4Sim is

signal Clk :  STD_LOGIC:='0';
signal Rst : STD_LOGIC:='0';
signal En : STD_LOGIC:='0';
signal Num : STD_LOGIC_VECTOR (3 downto 0):="0000";
constant CLK_PERIOD : TIME := 10 ns;

begin

DUT  :entity WORK.num4 port map(Clk=>Clk,Rst=>Rst,En=>En,Num=>Num);
 
 gen_clk: process
    begin
 Clk <= '0';
 wait for (CLK_PERIOD/2);
 Clk <= '1';
 wait for (CLK_PERIOD/2);
    end process gen_clk;
 
test: process
 variable RezCorect : STD_LOGIC_VECTOR(3 downto 0); 
 variable NrErori : INTEGER; 

 begin 
 RezCorect := "0000";
 NrErori := 0;
 
  Rst <= '1';
 wait for 10 ns;
 Rst <= '0';
 wait for 10 ns;
 En <= '1';
 
 for i in 0 to 15 loop 
   if Num /= RezCorect then
    report "Rezultat asteptat (" &
    STD_LOGIC'image (RezCorect(0)) & 
    STD_LOGIC'image (RezCorect(1)) &
    STD_LOGIC'image (RezCorect(2)) &
    STD_LOGIC'image (RezCorect(3)) &
    ") /= Valoare obtinuta (" &
    STD_LOGIC'image (Num(0)) & 
    STD_LOGIC'image (Num(1)) &
    STD_LOGIC'image (Num(2)) &
    STD_LOGIC'image (Num(3)) &
    ") la t = " & TIME'image (now)
    severity ERROR;
    NrErori := NrErori +1;
    end if;

 wait for 10 ns; 
 RezCorect := RezCorect+1;
  end loop;
 report "Testare terminata cu " &
   INTEGER'image (NrErori) & " erori";
end process;

end Behavioral;
