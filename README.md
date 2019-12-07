# Base Convert Pack
A utility datapack that allows you to do base conversions with a configurable base value

before you get started run the setup functions: 
> /function base_conv:setup
> /function rev_conv:setup

###  Decimal to base(x)
to set the base value use: 
> /scoreboard players set base= base_conv.num <number>
  
to set the input value use: 
> /scoreboard players set in= base_conv.num <number>

to run the conversion run:
> /function base_conv:call

you will get your output as an array in `storage base_conv:main out`
> example: in= 42, base= 2; will output as [1, 0, 1, 0, 1, 0]

###  base(x) to Decimal
to set the base value use: 
> /scoreboard players set base= rev_conv.num <number>

to set your input value use:
> /data modify storage rev_conv:main in set value [<array of numbers>]

to run the conversion run:
> /function base_conv:call

you will get your output in the scorboard value `out= rev_conv.num`
> example: {in:[8, 0]}, base= 16; will output as 128
