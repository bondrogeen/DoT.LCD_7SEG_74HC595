# DoT
 
The plugin 7-segment indicators on shift registers 74hc595 for [DoT](https://github.com/bondrogeen/DoT)

![Logo](https://raw.githubusercontent.com/bondrogeen/LCD_7SEG_74HC595/master/doc/Screenshot_1.jpg)

or manual 

```lua 

--initialization 
t={}
t.latch=6 -- pin of the shift register latch 74hc595
t.qty=6  -- number of shift registers 74hc595
t.type=false -- (optional def. false)  true = common cathode, false = common anode
t.speed=1000 -- (optional def. 500)
dofile("LCD_7SEG_74HC595.lua")({init=t})


-- Send a number.
dofile("LCD_7SEG_74HC595.lua")({set="123456"})

-- Send a number with a shift.
dofile("LCD_7SEG_74HC595.lua")({step="012345",speed=500}) -- speed - (optional)

-- Send a number with a shift. After completion, the callback function is executed
dofile("LCD_7SEG_74HC595.lua")({step="123456"},function(t)
print(t)
end)

```

![schematic](https://raw.githubusercontent.com/bondrogeen/LCD_7SEG_74HC595/master/doc/schematic.jpg)


[GitHub](http://github.com)

## Changelog

### 0.0.1 (2018-08-11)
* (bondrogeen) init.



