## Vanillio
Vanillio is a Destroy the Monument style map. The objective is to destroy the enemy team's obsidian monument.

This map features portals, which adds to the complexity of the XML. 

```xml
<map>
    <name>Vanillio</name>
    <version>1.0.0</version>
    <objective>Kill the enemy team to score points. First team to 50 points wins.</objective>
    <timeLimit>20m</timeLimit>

    <authors>
        <!-- Pixelific -->
        <author uuid="db3e4ab9-7c34-4342-8aca-63db60ec8d1b"/>
    </authors>

    <scoreboard>
        <team id="blue"/>
        <objective id="blue-monument"/>
        <space/>
        <team id="red"/>
        <objective id="red-monument"/>
    </scoreboard>

    <objectives>
        <objective team="blue" objective="red-monument"/>
        <objective team="red" objective="blue-monument"/>
    </objectives>

    <teams>
        <team id="blue" color="blue" max="15">Blue Team</team>
        <team id="red" color="red" max="15">Red Team</team>
    </teams>

    <spawns>
        <spawn team="observers" yaw="90">
            <cylinder base="25, 86, 14" height="1" radius="4"/>
        </spawn>

        <spawn team="blue" yaw="-180" kit="blue-kit">
            <block location="-28, 33, 87"/>
        </spawn>

        <spawn team="red" yaw="0" kit="red-kit">
            <block location="-28, 33, -58"/>
        </spawn>
    </spawns>

    <destroyables>
        <!-- Blue -->
        <destroyable id="blue-monument" name="Blue Monument" material="obsidian" health="3">
            <cylinder base="-28, 38, 131" radius="2" height="4"/>
        </destroyable>

        <!-- Red -->
        <destroyable id="red-monument" name="Red Monument" material="obsidian" health="3">
            <cylinder base="-28, 38, -100" radius="2" height="4"/>
        </destroyable>
    </destroyables>

    <filters>
        <filter modify="deny-all" message="You cannot modify team spawns!">
            <!-- Blue Top -->
            <cylinder base="-28, 30, 87" radius="6" height="20"/>

            <!-- Blue Bottom -->
            <cuboid min="-33, 23, 77" max="-23, 40, 63"/>

            <!-- Red Top -->
            <cylinder base="-28, 30, -58" radius="6" height="20"/>

            <!-- Red Bottom -->
            <cuboid min="-33, 23, -47" max="-23, 40, -31"/>
        </filter>
    </filters>

    <portals>
        <!-- Red -->
        <block id="red-destination" location="-28, 24, -43"/>
        <portal destination="red-destination" yaw="0">
            <cuboid min="-27, 33, -54" max="-29, 36, -53"/>
        </portal>

        <!-- Blue -->
        <block id="blue-destination" location="-28, 24, 74"/>
        <portal destination="blue-destination" yaw="180">
            <cuboid min="-30, 33, 83" max="-27, 36, 82"/>
        </portal>
    </portals>

     <kits>
    	<kit id="spawn">
            <item slot="0" material="stone sword"/>
            <item slot="1" material="bow"/>
            <item slot="2" material="diamond pickaxe"/>
            <enchantment id="dig speed"/>
            <item slot="3" material="iron axe"/>
            <item slot="4" material="log" amount="64"/>
            <item slot="5" material="vine" amount="32"/>
            <item slot="8" material="cooked beef" amount="32"/>
            <item slot="15" material="arrow" amount="16"/>
    	</kit>

        <kit id="red-kit" parents="spawn">
        	<helmet material="iron helmet"/>
            <chestplate material="leather chestplate" color="FF0000"/>
            <leggings material="leather leggings" color="FF0000"/>
            <boots material="leather boots" color="FF0000"/>
        </kit>

        <kit id="blue-kit" parents="spawn">
        	<helmet material="iron helmet"/>
            <chestplate material="leather chestplate" color="245BFA"/>
            <leggings material="leather leggings" color="245BFA"/>
            <boots material="leather boots" color="245BFA"/>
        </kit>
    </kits>
</map>
```
