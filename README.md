
# RaidCrawler Filters

A collection of RaidCrawler (batch) filters for specific use cases, provided by various members of the community.

A batch filter will result in one single clickable filter that can match multiple Pokémon. The preset filters.json files will result in various seperate filters.

To use the batch filters, simply copy the text contents and paste them into the Batch Filter textbox in RaidCrawler. To use the preset filter files, simply copy the contents of the filter and paste it into your filters.json located in your RaidCrawler folder.
## What are batch filters?

With a batch filter, it is possible to set multiple matches by excluding Pokémon you don't want to find, all while using a singular filter.

This works by ignoring Pokémon listed in the Batch Filters section via `!Species=<name>` syntax, where `<name>` is the species' name based on [PKHeX's recognized names list](<https://github.com/kwsch/PKHeX/blob/master/PKHeX.Core/Game/Enums/Species.cs>).

*Note: When using names, some will need to be changed to include their special characters or spaces such as `Nidoran♀`, `Iron Hands`, `Mr. Mime`, `Farfetch’d`, and so on.*
*Alternatively, you can use the Pokémon's # position in the Species.cs list as well, where None counts as 0. Example: to exclude Nidoran♀, you would use `!Species=29`*.

For specific forms, you'll have to ignore the Pokémon in the batch filter, and then make a separate filter that matches the form you want. 

Credit to Sock for the above explanation.

## List of batch filters

- [Teal Mask Only](https://pastebin.com/XTL8vhMG) - credit to Sock
- [Indigo Disk Only](https://github.com/ilihasj/rcfilters/blob/a8d14204b021cbdc5152e52e3fdfc4d62d15ab6f/Blueberry_Filter.txt) - credit to Newt
- [Gender Differences](https://github.com/ilihasj/rcfilters/blob/a8d14204b021cbdc5152e52e3fdfc4d62d15ab6f/Gender_Differences.txt)
- [Violet Exclusives](https://github.com/ilihasj/rcfilters/blob/a8d14204b021cbdc5152e52e3fdfc4d62d15ab6f/Violet_Exclusives.txt)
- [Scarlet Exclusives](https://github.com/ilihasj/rcfilters/blob/a8d14204b021cbdc5152e52e3fdfc4d62d15ab6f/Scarlet_Exclusives.txt)

## List of preset filters

- [Master Filter (All Pokémon, Gender Differences, Alphabetical Order)](https://github.com/ilihasj/rcfilters/blob/236fdb44e1fa79731dba43fd3afd5f42eba70225/filters_master_zrvaeal.json) - credit to zrvaeal
- [Indigo Disk species](https://github.com/ilihasj/rcfilters/blob/a8d14204b021cbdc5152e52e3fdfc4d62d15ab6f/Indigo_Disk.json) - credit to Newt
- [Only DLC Pokémon + Gender Differences](https://github.com/ilihasj/rcfilters/blob/a8d14204b021cbdc5152e52e3fdfc4d62d15ab6f/DLC_Gender.json) - credit to Hyrula
- [All Available Raids](https://github.com/ilihasj/rcfilters/blob/a8d14204b021cbdc5152e52e3fdfc4d62d15ab6f/All_Raids.json) - credit to Don

## Size Batch Filters

Similar to excluding Pokémon, you can also use batch filters to look for specific sizes.

|Group  |  Size Value 
--------|---------- 
XXXL |   255  
XXL  |  231-254
XL    |    196-230
L      |  156-195
M       | 100-155
S      |  60-99
XS     |   25-59
XXS  | 1-24
XXXS   | 0

### Example use cases

**XXXS Only**
`=Scale=0`

**XXXL Only** `=Scale=255`

**XXS or smaller**
`≤Scale=24`

**XXL or larger**
`≥Scale=231`

**XL range only**```≥Scale=196 ≤Scale=230```

Adjust the values above as needed and place them in the "Batch Filters" text box of your filter.

Once again, credit to Sock for the above explanation. The data on sizing was sourced from [Serebii](https://www.serebii.net/scarletviolet/size.shtml). 
