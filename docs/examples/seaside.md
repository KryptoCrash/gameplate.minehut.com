## Seaside Circuit
Seaside Circuit is a TDM style map with Goal regions that players can jump through to gain points. 

This map highlights the `Goals` score type.

```xml
<map>
    <name>Seaside Circuit</name>
    <version>1.0.0</version>
    <objective>Kill the enemy team to score points. First team to 50 points wins.</objective>
    <timeLimit>5m</timeLimit>

    <authors>
        <!-- Pixelific -->
        <author uuid="db3e4ab9-7c34-4342-8aca-63db60ec8d1b"/>
    </authors>

    <score>
        <limit>50</limit>
        <kill>1</kill>

        <goal team="red" amount="3">
            <cuboid min="-14, 1, 14" max="-16, 2, 16"/>
        </goal>
        <goal team="red" amount="5">
            <cuboid min="-49, 4, 1" max="-51, 5, -1"/>
        </goal>

        <goal team="blue" amount="3">
            <cuboid min="56, 1, 14" max="54, 2, 16"/>
        </goal>
        <goal team="blue" amount="5">
            <cuboid min="91, 4, -1" max="89, 5, 1"/>
        </goal>
    </score>

    <scoreboard>
        <objective id="scores"/>
    </scoreboard>

    <teams>
        <team id="blue" color="blue" max="15">Blue Team</team>
        <team id="red" color="red" max="15">Red Team</team>
    </teams>

    <spawns>
        <spawn team="observers" yaw="-180">
            <cylinder base="20, 76, 73" height="1" radius="3"/>
        </spawn>

        <spawn team="blue" yaw="-115" kit="blue-kit">
            <cylinder base="-54, 3, 56" radius="2" height="1"/>
        </spawn>

        <spawn team="red" yaw="115" kit="red-kit">
            <cylinder base="95, 3, 56" radius="2" height="1"/>
        </spawn>
    </spawns>

    <filters>
        <filter modify="deny-all">
            <region id="global"/>
        </filter>
    </filters>

     <kits>
    	<kit id="spawn">
            <item slot="0" material="stone sword"/>
            <item slot="1" material="bow">
                <enchantment id="arrow infinite"/>
            </item>
            <item slot="8" material="cooked beef" amount="32"/>
            <item slot="15" material="arrow" amount="1"/>
            <item slot="2" material="golden apple" amount="1"/>
    	</kit>

        <kit id="red-kit" parents="spawn">
        	<helmet material="leather helmet" color="FF0000"/>
            <chestplate material="leather chestplate" color="FF0000"/>
            <leggings material="leather leggings" color="FF0000"/>
            <boots material="leather boots" color="FF0000"/>
        </kit>

        <kit id="blue-kit" parents="spawn">
        	<helmet material="leather helmet" color="245BFA"/>
            <chestplate material="leather chestplate" color="245BFA"/>
            <leggings material="leather leggings" color="245BFA"/>
            <boots material="leather boots" color="245BFA"/>
        </kit>
    </kits>
</map>
```