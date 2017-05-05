# Cape Trader
Cape Trader is used to automate the process of augmenting ambuscade capes. The cape trader addon injects packets extensively so please take that into consideration and use this addon at you own risk. While there are some safeguards in this addon, there is still a risk that you can lose your abdhaljs thread,dust,sap and dye if you use this addon. Please read the usage notes and information on the prep and go commands carefully as well as the warnings section before deciding to use this addon.

___
#### Usage notes


After downloading, to use capetrader you must first unzip the folder in your addons folder. Be sure to rename this folder to capetrader.

Load the addon by using the following command:

    //lua load capetrader

There are some conditions that you need to meet in order to use the important go and prep commands. Points 4 and 5 are particularly important to consider:

1. You must be in Mhaura and be within a distance of 6 to the Gorpa-Masorpa npc.

2. If you have only recently zoned into Mhaura make sure your inventory has completely finished loading before using the go command.

3. Make sure there is only one of the given cape you want to augment in your inventory. For example if you are intending to augment an ogma's cape, there should only be one ogma's cape in your inventory.

4. The go command takes a number as an input that represents the number of times you wish to augment your cape. It is possible you will lose your thread,dust,sap and dye if you enter a number that would take your augment past its possible maximum. For example suppose you have an ogma's cape already augmented with Dex+5 from a thread item. After using the **//ct prep thread ogma's cape dex** command you enter **//ct go 20** command. There is a safeguard that will stop the augmentation process after augmenting your cape 15 times. **However, there is NO guarantee this safeguard will work for every possible augment path. Particularly pet related paths that I have not yet been able to test.** It is highly recommended that you enter the exact number of times you need to max a particular path to decrease the chance of lost items.

5. It is also possible to lose augment items if you try to augment a cape with a different path than is already present. Suppose again you have an ogma's cape augmented with DEX+5 via threads. If you enter the **//ct prep thread ogma's cape str** and then the **//ct go 15** command intending to augment your cape with str, **you will lose all 15 threads**. There is currently no safeguard for this but one is currently being considered to be added to the capetrader addon.

6. If you have the inventory menu open, be sure to close before using the go commmand and make sure you do not open menus or move items around in your inventories while the augmentation process is ongoing. You will get a start message after you use the go command and an ending message once the augmentation process completes. You can mess around with your inventory after you get the ending message, otherwise you will interupt the augmentation process.


Suppose you want to augment an ogma's cape from scratch with dex, accuracy and attack, and double attack. You can use the following steps:

1.	Enter //ct prep thread ogma's cape dex

2.	Enter //ct go 20

3. Wait for the ending message

4. Enter //ct prep dust ogma's cape acc/atk

5. Enter //ct go 20

6.	Wait for the ending message.

7. Enter //ct prep sap ogma's cape doubleattack

8.	Enter //ct go 10

9. Upon receiving the completion message you can then consider augmenting another cape.

___

#### Commands

The **help** command displays all of the possible commands of CapeTrader in your chat windower. Below are the equivalent ways of calling the command:

    //ct help
    //ct h
    //capetrader help
    //capetrader h

The **reload** command reloads the addon. Useful if you ever the addon ever getting stuck in the augmentation process. The below are equivalent:

    //ct reload
    //ct r
    //capetrader reload
    //capetrader r

The **unload** command reloads the addon. Useful if you ever the addon ever getting stuck in the augmentation process or want to unload the addon quickly. The below are equivalent:

    //ct unload
    //ct u
    //capetrader unload
    //capetrader u

The **prep** command is one of the key components of this addon's function. This command tells the go command how to augment your cape. There are three inputs to the prep command. First is the type of augment item: thread, dust, sap and dye. Second is the name of the cape, for example: camulus's mantle. Third is the augment path. Note that none of these inputs are case sensitive. Also in case you are not sure exactly what to input for the augment path input, you can use the list command or use the following list for reference. Below are all of the possible ways to prepare a camulus's mantle:

    //ct prep thread camulus's mantle hp
    //ct prep thread camulus's mantle mp
    //ct prep thread camulus's mantle str
    //ct prep thread camulus's mantle dex
    //ct prep thread camulus's mantle vit
    //ct prep thread camulus's mantle agi
    //ct prep thread camulus's mantle int
    //ct prep thread camulus's mantle mnd
    //ct prep thread camulus's mantle chr
    //ct prep thread camulus's mantle petmelee
    //ct prep thread camulus's mantle petmagic

    //ct prep dust camulus's mantle acc/atk
    //ct prep dust camulus's mantle racc/ratk
    //ct prep dust camulus's mantle macc/mdmg
    //ct prep dust camulus's mantle eva/meva

    //ct prep sap camulus's mantle wsd
    //ct prep sap camulus's mantle critrate
    //ct prep sap camulus's mantle stp
    //ct prep sap camulus's mantle doubleattack
    //ct prep sap camulus's mantle haste
    //ct prep sap camulus's mantle dw
    //ct prep sap camulus's mantle enmity+
    //ct prep sap camulus's mantle enmity-
    //ct prep sap camulus's mantle snapshot
    //ct prep sap camulus's mantle mab
    //ct prep sap camulus's mantle fc
    //ct prep sap camulus's mantle curepotency
    //ct prep sap camulus's mantle waltzpotency
    //ct prep sap camulus's mantle petregen
    //ct prep sap camulus's mantle pethaste

    //ct prep dye camulus's mantle hp
    //ct prep dye camulus's mantle mp
    //ct prep dye camulus's mantle str
    //ct prep dye camulus's mantle dex
    //ct prep dye camulus's mantle vit
    //ct prep dye camulus's mantle agi
    //ct prep dye camulus's mantle int
    //ct prep dye camulus's mantle mnd
    //ct prep dye camulus's mantle chr
    //ct prep dye camulus's mantle acc
    //ct prep dye camulus's mantle atk
    //ct prep dye camulus's mantle racc
    //ct prep dye camulus's mantle ratk
    //ct prep dye camulus's mantle macc
    //ct prep dye camulus's mantle mdmg
    //ct prep dye camulus's mantle eva
    //ct prep dye camulus's mantle meva
    //ct prep dye camulus's mantle petacc
    //ct prep dye camulus's mantle petatk
    //ct prep dye camulus's mantle petmacc
    //ct prep dye camulus's mantle petmdmg

The **go** command is the second key component of the CapeTrader addon and requires that you have used the prep command correctly beforehand. Remember again that using this command carries with it some risks as described in the usage notes section. If you do not provide an input the go command will by default only augment your cape once. Below are equivalent ways of augmenting your cape 20 times:

    //ct go 20
    //capetrader go 20

The **list** command is used as a reminder of what are valid inputs for the augmentpath input of the prep command. Below are the equivalent ways of calling this command:

    //ct list
    //capetrader list
    //ct l
    //capetrader l
___


#### Warnings and notes on the relevant packets
There are four parts to the process of augmenting your ambuscade cape:

1. Part 1: Targetting gorpa-masorpa plus putting together and trading the relevant items. This takes me about 10 seconds to complete. (Involves outgoing packet 0x036)

2. Part 2: Waiting for the dialog menu to pop up and become usable. This takes about 1 second and can't be controlled by the player. (Involves the incoming 0x034 packet.)

3. Part 3: Navigating the menu to confirm and augment your cape. This takes me 2-3 seconds to confirm. (Involves 2 outgoing 0x05B packets)

4. Part 4: Waiting and receiving your newly augmented cape back. This takes anywhere from 1 to 3 seconds and can't be controlled by the player. (Involves the incoming 0x01D packet)

The cape trader addon uses packets in order to substantially speed up parts one and three from above at a speed that would not normally be possible. Therefore if you use this addon you could potentially look suspicious. Part 1 of the process takes only 1 second using this addon. If this makes you uncomfortable you can change the value of the TRADE_DELAY variable in the capeTrader.lua file to a more reasonable amount if you wish. This addon does part 3 pretty much instantaneously once the incoming 0x034 packet is received from part 2. So once again you can look suspicious again during this stage. There is currently no option to add a delay to this at the moment but it is being considered to have such a delay. The time it takes for part 2 and 4 should not be that different from you augmenting capes manually.

The possibility of the loss of augment items comes from part 3. When augmenting normally you will get denied by the npc if you try to trade an already maxed cape. Injecting the 0x036 packet and later the 0x05B packets bypasses this check but you lose your augment items but get your cape back unchanged if you have already maxed an augment path. There are some safeguards to prevent this happening in this addon but it has not been tested on every single augment path. So please use the go command with caution.

Please keep all of the above in mind before deciding to use this addon. If you do decide to use CapeTrader I hope you find it useful!
