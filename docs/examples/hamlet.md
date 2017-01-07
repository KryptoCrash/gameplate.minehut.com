## Hamlet
Hamlet is an Attack/Defend map. The objective is for the attackers to destroy the monument guarded by the defenders. 

This map highlights the possibility to define a winner when the time limit has been reached.

{% highlight xml %}
```xml
<map>
    <name>Hamlet</name>
    <version>1.0.0</version>
    <objective>The attackers have 10 minutes to destroy the Monument. The defenders must stop them!</objective>
    <timeLimit team="defenders">10m</timeLimit>

    <authors>
        <!-- Pixelific -->
        <author uuid="db3e4ab9-7c34-4342-8aca-63db60ec8d1b"/>
        <!-- Fruuitss -->
        <author uuid="2000269b-1340-4e63-9517-ecae2f868df8"/>
        <!-- etmfrederick -->
        <author uuid="d97d56b5-15bc-4469-ac21-bc3a73f9dd89"/>
    </authors>

    <contributors>
        <!-- Luuke -->
        <contributor uuid="2dc9b2a1-6063-499b-9685-aa97b978707a" contribution="Map Layout and XML help."/>
    </contributors>

    <scoreboard>
        <space/>
        <objective id="defenders-monument"/>
        <space/>
    </scoreboard>

    <objectives>
        <objective team="attackers" objective="defenders-monument"/>
    </objectives>

    <teams>
        <team id="defenders" color="blue" max="15">Defenders</team>
        <team id="attackers" color="red" max="15">Attackers</team>
    </teams>

    <spawns>
        <spawn team="observers" yaw="0">
            <cylinder base="-48, 69, -31" height="1" radius="4"/>
        </spawn>

        <spawn team="defenders" yaw="-135" kit="defenders-kit">
            <block location="-77, 18, 164"/>
        </spawn>

        <spawn team="attackers" yaw="0" kit="attackers-kit">
            <block location="-46, 10, -17"/>
        </spawn>
    </spawns>

    <destroyables>
        <destroyable id="defenders-monument" name="Monument" material="obsidian" health="2">
            <cylinder base="-15, 16, 152" radius="2" height="8"/>
        </destroyable>
    </destroyables>

    <filters>
        <filter modify="deny-all" message="You cannot modify team spawns!">
            <!-- Defender -->
            <cylinder base="-77, 15, 164" radius="20" height="40"/>

            <!-- Attacker -->
            <cuboid min="-63, 7, 2" max="-30, 38, -31"/>
        </filter>
    </filters>

     <kits>
    	<kit id="spawn">
            <item slot="0" material="stone sword"/>
            <item slot="15" material="arrow" amount="16"/>
            <item slot="1" material="bow"/>
            <item slot="2" material="iron axe"/>

            <item slot="4" material="log" amount="32"/>

            <item slot="7" material="golden apple"/>
            <item slot="8" material="cooked fish" amount="32"/>
    	</kit>

        <kit id="attackers-kit" parents="spawn">

            <item slot="3" material="diamond pickaxe"/>
            <item slot="5" material="ladder" amount="32"/>

        	<helmet material="leather helmet" color="FF0000"/>
            <chestplate material="leather chestplate" color="FF0000"/>
            <leggings material="leather leggings" color="FF0000"/>
            <boots material="leather boots" color="FF0000"/>
        </kit>

        <kit id="defenders-kit" parents="spawn">
        	<helmet material="iron helmet"/>
            <chestplate material="leather chestplate" color="245BFA"/>
            <leggings material="iron leggings"/>
            <boots material="leather boots" color="245BFA"/>
        </kit>
    </kits>
</map>
```
{% endhighlight %}