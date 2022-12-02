# Experiment

## Settings

We evaluate our PED method, both the global path-encoding-based strategy, PEDG, and decomposed path-encoding-based strategy, PEDD, on various compositional hybrid systems, all involving discontinuous behavior that cannot be solved by gradient-based methods. Our approach is implemented in Java and all the experiments are conducted on the same PC (Intel Core i7 2.30GHz, 32GB RAM, Windows 10).

Our approach is evaluated on three different systems, the robotic arm systems(marked as Arm), quadcopter drone systems (marked as Drone), and three different vehicle systems, with respect to different scenarios of the straight road (Veh-a), crossroad (Veh-b), and T-junction (Veh-c). 

## File description
In [models](../models/models.zip), we have 30 files and can be divided into two categories, ```xml``` files and ```cfg``` files.  ```xml``` files describe the automata of systems, and ```cfg``` files detail the following infomation:

<ul>
<li>system: the name of system</li>
<li>initially: the initial parameters value or range</li>
<li>target_x: the target position in X axis</li>
<li>target_y: the target position in Y axis</li>
<li>(Optional) target_z : the target position in Z axis</li>
<li>obj_function: the objective function</li>
</ul>

For example, ```Drone.xml``` gives the automaton of a quadcopter drone system and ```Drone-2.cfg``` gives the information of the second component in drone system.

For each scenario, we set the number of components in the system as $1$, $2$, $3$ and $5$ respectively. For example, Arm-2 stands for the robotic arm system with first two components, ```Arm-1.cfg``` and ```Arm-2.cfg``` , while Drone-5 stands for the system with all five drones.

# Results

<table class="tg">
<thead>
  <tr>
    <th class="tg-9wq8">　</th>
    <th class="tg-9wq8" colspan="3">Success rate (%)</th>
    <th class="tg-9wq8" colspan="3">Time&nbsp;&nbsp;&nbsp;cost (s)</th>
    <th class="tg-c3ow" colspan="2">Memory cost (MB)</th>
    <th class="tg-9wq8" colspan="2">Simulation&nbsp;&nbsp;&nbsp;rounds</th>
    <th class="tg-9wq8" colspan="3">Optimization&nbsp;&nbsp;&nbsp;value</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-9wq8">Benchmark</td>
    <td class="tg-9wq8">CDH</td>
    <td class="tg-9wq8">PEDG </td>
    <td class="tg-9wq8">PEDD</td>
    <td class="tg-9wq8">CDH</td>
    <td class="tg-9wq8">PEDG</td>
    <td class="tg-9wq8">PEDD</td>
    <td class="tg-9wq8">PEDG</td>
    <td class="tg-9wq8">PEDD</td>
    <td class="tg-9wq8">PEDG</td>
    <td class="tg-9wq8">PEDD</td>
    <td class="tg-9wq8">CDH</td>
    <td class="tg-9wq8">PEDG</td>
    <td class="tg-9wq8">PEDD</td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Arm-1.zip">Arm-1</td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-9wq8">41.20 </td>
    <td class="tg-9wq8">12.89 </td>
    <td class="tg-uzvj">2.25 </td>
    <td class="tg-9wq8">371.55 </td>
    <td class="tg-uzvj">347.44 </td>
    <td class="tg-9wq8">819.53 </td>
    <td class="tg-uzvj">420.12 </td>
    <td class="tg-9wq8">-9999.1 </td>
    <td class="tg-9wq8">-9997.4 </td>
    <td class="tg-9wq8">-9996.3 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Arm-2.zip">Arm-2</td>
    <td class="tg-9wq8">0 </td>
    <td class="tg-9wq8">98 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">79.41 </td>
    <td class="tg-uzvj">71.70 </td>
    <td class="tg-9wq8">389.64 </td>
    <td class="tg-uzvj">367.22 </td>
    <td class="tg-uzvj">15315.36 </td>
    <td class="tg-9wq8">15761.64 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">-19991.2 </td>
    <td class="tg-9wq8">-19989.6 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Arm-3.zip">Arm-3</td>
    <td class="tg-9wq8">0 </td>
    <td class="tg-9wq8">95 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">183.22 </td>
    <td class="tg-uzvj">80.89 </td>
    <td class="tg-9wq8">414.21 </td>
    <td class="tg-uzvj">396.15 </td>
    <td class="tg-9wq8">26747.39 </td>
    <td class="tg-uzvj">16392.65 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">-29977.2 </td>
    <td class="tg-9wq8">-29990.9 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Arm-5.zip">Arm-5</td>
    <td class="tg-9wq8">0 </td>
    <td class="tg-9wq8">93 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">891.77 </td>
    <td class="tg-uzvj">90.21 </td>
    <td class="tg-9wq8">679.36 </td>
    <td class="tg-uzvj">453.68 </td>
    <td class="tg-9wq8">35479.47 </td>
    <td class="tg-uzvj">19203.20 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">-49985.6 </td>
    <td class="tg-9wq8">-49989.6 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Veh-a-1.zip">Veh-a-1</td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-9wq8">80.45 </td>
    <td class="tg-9wq8">10.41 </td>
    <td class="tg-uzvj">1.82 </td>
    <td class="tg-9wq8">210.29 </td>
    <td class="tg-uzvj">187.84 </td>
    <td class="tg-9wq8">271.91 </td>
    <td class="tg-uzvj">82.39 </td>
    <td class="tg-9wq8">-9995.6 </td>
    <td class="tg-9wq8">-9989.2 </td>
    <td class="tg-9wq8">-9993.7 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Veh-a-2.zip">Veh-a-2</td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-9wq8">99 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-9wq8">1913.24 </td>
    <td class="tg-9wq8">69.73 </td>
    <td class="tg-uzvj">45.25 </td>
    <td class="tg-uzvj">256.91 </td>
    <td class="tg-9wq8">258.45 </td>
    <td class="tg-9wq8">2297.60 </td>
    <td class="tg-uzvj">1657.12 </td>
    <td class="tg-9wq8">-19993.5 </td>
    <td class="tg-9wq8">-19991.2 </td>
    <td class="tg-9wq8">-19995.4 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Veh-a-3.zip">Veh-a-3</td>
    <td class="tg-9wq8">19 </td>
    <td class="tg-9wq8">94 </td>
    <td class="tg-uzvj">96 </td>
    <td class="tg-9wq8">3406.64 </td>
    <td class="tg-9wq8">334.64 </td>
    <td class="tg-uzvj">234.46 </td>
    <td class="tg-9wq8">268.02 </td>
    <td class="tg-uzvj">222.69 </td>
    <td class="tg-9wq8">5695.50 </td>
    <td class="tg-uzvj">2761.90 </td>
    <td class="tg-9wq8">-29985.2 </td>
    <td class="tg-9wq8">-29969.3 </td>
    <td class="tg-9wq8">-29979.5 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Veh-a-5.zip">Veh-a-5</td>
    <td class="tg-9wq8">0 </td>
    <td class="tg-9wq8">62 </td>
    <td class="tg-uzvj">74 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">2611.57 </td>
    <td class="tg-uzvj">1885.80 </td>
    <td class="tg-9wq8">273.65 </td>
    <td class="tg-uzvj">236.07 </td>
    <td class="tg-9wq8">11288.70 </td>
    <td class="tg-uzvj">7218.55 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">-49936.5 </td>
    <td class="tg-9wq8">-49983.7 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Veh-b-1.zip">Veh-b-1</td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-9wq8">8.31 </td>
    <td class="tg-9wq8">4.24 </td>
    <td class="tg-uzvj">1.98 </td>
    <td class="tg-9wq8">210.11 </td>
    <td class="tg-uzvj">183.53 </td>
    <td class="tg-9wq8">102.38 </td>
    <td class="tg-uzvj">97.29 </td>
    <td class="tg-9wq8">-9994.2 </td>
    <td class="tg-9wq8">-9997.3 </td>
    <td class="tg-9wq8">-9995.3 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Veh-b-2.zip">Veh-b-2</td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-9wq8">1502.40 </td>
    <td class="tg-9wq8">78.52 </td>
    <td class="tg-uzvj">41.14 </td>
    <td class="tg-9wq8">249.25 </td>
    <td class="tg-uzvj">212.44 </td>
    <td class="tg-9wq8">3814.20 </td>
    <td class="tg-uzvj">1934.38 </td>
    <td class="tg-9wq8">-19999.2 </td>
    <td class="tg-9wq8">-19998.3 </td>
    <td class="tg-9wq8">-19996.8 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Veh-b-3.zip">Veh-b-3</td>
    <td class="tg-9wq8">53 </td>
    <td class="tg-9wq8">89 </td>
    <td class="tg-uzvj">96 </td>
    <td class="tg-9wq8">2961.63 </td>
    <td class="tg-9wq8">417.35 </td>
    <td class="tg-uzvj">217.18 </td>
    <td class="tg-9wq8">259.43 </td>
    <td class="tg-uzvj">192.26 </td>
    <td class="tg-9wq8">8614.70 </td>
    <td class="tg-uzvj">3276.20 </td>
    <td class="tg-9wq8">-29990.8 </td>
    <td class="tg-9wq8">-29984.1 </td>
    <td class="tg-9wq8">-29981.4 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Veh-b-5.zip">Veh-b-5</td>
    <td class="tg-9wq8">0 </td>
    <td class="tg-9wq8">61 </td>
    <td class="tg-uzvj">91 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">2478.92 </td>
    <td class="tg-uzvj">538.47 </td>
    <td class="tg-9wq8">276.80 </td>
    <td class="tg-uzvj">210.46 </td>
    <td class="tg-9wq8">14201.40 </td>
    <td class="tg-uzvj">4010.20 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">-49985.2 </td>
    <td class="tg-9wq8">-49990.4 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Veh-c-1.zip">Veh-c-1</td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-9wq8">33.76 </td>
    <td class="tg-9wq8">6.18 </td>
    <td class="tg-uzvj">2.28 </td>
    <td class="tg-9wq8">264.36 </td>
    <td class="tg-uzvj">193.21 </td>
    <td class="tg-9wq8">593.63 </td>
    <td class="tg-uzvj">128.09 </td>
    <td class="tg-9wq8">-9998.4 </td>
    <td class="tg-9wq8">-9999.4 </td>
    <td class="tg-9wq8">-9996.8 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Veh-c-2.zip">Veh-c-2</td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-9wq8">1834.68 </td>
    <td class="tg-9wq8">50.43 </td>
    <td class="tg-uzvj">30.08 </td>
    <td class="tg-9wq8">243.98 </td>
    <td class="tg-uzvj">228.95 </td>
    <td class="tg-9wq8">2189.30 </td>
    <td class="tg-uzvj">1870.00 </td>
    <td class="tg-9wq8">-19996.1 </td>
    <td class="tg-9wq8">-19992.2 </td>
    <td class="tg-9wq8">-19987.8 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Veh-c-3.zip">Veh-c-3</td>
    <td class="tg-9wq8">45 </td>
    <td class="tg-9wq8">95 </td>
    <td class="tg-uzvj">99 </td>
    <td class="tg-9wq8">3519.77 </td>
    <td class="tg-9wq8">357.52 </td>
    <td class="tg-uzvj">121.15 </td>
    <td class="tg-9wq8">278.30 </td>
    <td class="tg-uzvj">235.30 </td>
    <td class="tg-9wq8">7287.00 </td>
    <td class="tg-uzvj">2715.03 </td>
    <td class="tg-9wq8">-29983.6 </td>
    <td class="tg-9wq8">-29979.1 </td>
    <td class="tg-9wq8">-29987.3 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Veh-c-5.zip">Veh-c-5</td>
    <td class="tg-9wq8">0 </td>
    <td class="tg-9wq8">76 </td>
    <td class="tg-uzvj">83 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">1127.56 </td>
    <td class="tg-uzvj">360.48 </td>
    <td class="tg-9wq8">321.60 </td>
    <td class="tg-uzvj">286.70 </td>
    <td class="tg-9wq8">21360.00 </td>
    <td class="tg-uzvj">8184.27 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">-49991.2 </td>
    <td class="tg-9wq8">-49984.4 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Drone-1.zip">Drone-1</td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-uzvj">100 </td>
    <td class="tg-9wq8">14.69 </td>
    <td class="tg-9wq8">3.47 </td>
    <td class="tg-uzvj">2.46 </td>
    <td class="tg-9wq8">367.87 </td>
    <td class="tg-uzvj">241.64 </td>
    <td class="tg-9wq8">593.10 </td>
    <td class="tg-uzvj">391.20 </td>
    <td class="tg-9wq8">-9988.5 </td>
    <td class="tg-9wq8">-9978.5 </td>
    <td class="tg-9wq8">-9985.9 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Drone-2.zip">Drone-2</td>
    <td class="tg-9wq8">0 </td>
    <td class="tg-9wq8">59 </td>
    <td class="tg-uzvj">63 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">2102.96 </td>
    <td class="tg-uzvj">1354.52 </td>
    <td class="tg-9wq8">379.33 </td>
    <td class="tg-uzvj">251.45 </td>
    <td class="tg-9wq8">8568.40 </td>
    <td class="tg-uzvj">5566.00 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">-19894.4 </td>
    <td class="tg-9wq8">-19976.6 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Drone-3.zip">Drone-3</td>
    <td class="tg-9wq8">0 </td>
    <td class="tg-9wq8">24 </td>
    <td class="tg-uzvj">35 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">2914.45 </td>
    <td class="tg-uzvj">2400.53 </td>
    <td class="tg-9wq8">492.14 </td>
    <td class="tg-uzvj">287.73 </td>
    <td class="tg-9wq8">28293.22 </td>
    <td class="tg-uzvj">19462.34 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">-29994.7 </td>
    <td class="tg-9wq8">-29985.1 </td>
  </tr>
  <tr>
    <td class="tg-9wq8"><a href="../models/Drone-5.zip">Drone-5</td>
    <td class="tg-9wq8">0 </td>
    <td class="tg-9wq8">18 </td>
    <td class="tg-uzvj">27 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">3497.25 </td>
    <td class="tg-uzvj">2695.32 </td>
    <td class="tg-9wq8">653.21 </td>
    <td class="tg-uzvj">325.66 </td>
    <td class="tg-9wq8">35821.00 </td>
    <td class="tg-uzvj">23715.00 </td>
    <td class="tg-9wq8">N/A</td>
    <td class="tg-9wq8">-49892.1 </td>
    <td class="tg-9wq8">-49940.3 </td>
  </tr>
</tbody>
</table>

