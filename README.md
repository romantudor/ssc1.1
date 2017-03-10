# ssc1.1
----------------------------------------------------------------------------------
-- Company: 
-- Engineer: 
-- 
-- Create Date: 03/10/2017 03:20:30 PM
-- Design Name: 
-- Module Name: conv - Behavioral
-- Project Name: 
-- Target Devices: 
-- Tool Versions: 
-- Description: 
-- 
-- Dependencies: 
-- 
-- Revision:
-- Revision 0.01 - File Created
-- Additional Comments:
-- 
----------------------------------------------------------------------------------


library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

-- Uncomment the following library declaration if using
-- arithmetic functions with Signed or Unsigned values
--use IEEE.NUMERIC_STD.ALL;

-- Uncomment the following library declaration if instantiating
-- any Xilinx leaf cells in this code.
--library UNISIM;
--use UNISIM.VComponents.all;

entity conv is
    Port ( num : in STD_LOGIC_VECTOR (0 downto 3);
           BCD1 : out STD_LOGIC_VECTOR (0 downto 3);
           BCD0 : out STD_LOGIC_VECTOR (0 downto 3));
end conv;

architecture Behavioral of conv is

begin

con: process
   variable y: STD_LOGIC_VECTOR(3 downto 0);
    begin
      C1: case y is
          when "0000" => BCD1 <= "0000"; BCD0<="0000"; --0
          when "0001" => BCD1 <= "0000"; BCD0<="0001"; --1
          when "0010" => BCD1 <= "0000"; BCD0<="0010"; --2
          when "0011" => BCD1 <= "0000"; BCD0<="0011"; --3
          when "0100" => BCD1 <= "0000"; BCD0<="0100"; --4
          when "0101" => BCD1 <= "0000"; BCD0<="0101"; --5
          when "0110" => BCD1 <= "0000"; BCD0<="0110"; --6
          when "0111" => BCD1 <= "0000"; BCD0<="0111"; --7
          when "1000" => BCD1 <= "0000"; BCD0<="1000"; --8
          when "1001" => BCD1 <= "0000"; BCD0<="1001"; --9
          when "1010" => BCD1 <= "0001"; BCD0<="0000"; --10
          when "1011" => BCD1 <= "0001"; BCD0<="0001"; --11
          when "1100" => BCD1 <= "0001"; BCD0<="0010"; --12
          when "1101" => BCD1 <= "0001"; BCD0<="0011"; --13
          when "1110" => BCD1 <= "0001"; BCD0<="0100"; --14
          when "1111" => BCD1 <= "0001"; BCD0<="0101"; --15
          when others => BCD1<="1111"; BCD1<="1111";                                
      end case C1;
    end process;
    

end Behavioral;









----------------------------------------------------------------------------------
-- Company: 
-- Engineer: 
-- 
-- Create Date: 03/10/2017 03:20:30 PM
-- Design Name: 
-- Module Name: conv - Behavioral
-- Project Name: 
-- Target Devices: 
-- Tool Versions: 
-- Description: 
-- 
-- Dependencies: 
-- 
-- Revision:
-- Revision 0.01 - File Created
-- Additional Comments:
-- 
----------------------------------------------------------------------------------


library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

-- Uncomment the following library declaration if using
-- arithmetic functions with Signed or Unsigned values
--use IEEE.NUMERIC_STD.ALL;

-- Uncomment the following library declaration if instantiating
-- any Xilinx leaf cells in this code.
--library UNISIM;
--use UNISIM.VComponents.all;

entity conv is
    Port ( num : in STD_LOGIC_VECTOR (0 downto 3);
           BCD1 : out STD_LOGIC_VECTOR (0 downto 3);
           BCD0 : out STD_LOGIC_VECTOR (0 downto 3));
end conv;

architecture Behavioral of conv is

begin

con: process
   variable y: STD_LOGIC_VECTOR(3 downto 0);
    begin
      C1: case y is
          when "0000" => BCD1 <= "0000"; BCD0<="0000"; --0
          when "0001" => BCD1 <= "0000"; BCD0<="0001"; --1
          when "0010" => BCD1 <= "0000"; BCD0<="0010"; --2
          when "0011" => BCD1 <= "0000"; BCD0<="0011"; --3
          when "0100" => BCD1 <= "0000"; BCD0<="0100"; --4
          when "0101" => BCD1 <= "0000"; BCD0<="0101"; --5
          when "0110" => BCD1 <= "0000"; BCD0<="0110"; --6
          when "0111" => BCD1 <= "0000"; BCD0<="0111"; --7
          when "1000" => BCD1 <= "0000"; BCD0<="1000"; --8
          when "1001" => BCD1 <= "0000"; BCD0<="1001"; --9
          when "1010" => BCD1 <= "0001"; BCD0<="0000"; --10
          when "1011" => BCD1 <= "0001"; BCD0<="0001"; --11
          when "1100" => BCD1 <= "0001"; BCD0<="0010"; --12
          when "1101" => BCD1 <= "0001"; BCD0<="0011"; --13
          when "1110" => BCD1 <= "0001"; BCD0<="0100"; --14
          when "1111" => BCD1 <= "0001"; BCD0<="0101"; --15
          when others => BCD1<="1111"; BCD1<="1111";                                
      end case C1;
    end process;
    

end Behavioral;
