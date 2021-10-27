# 802.15.4 wireless MAC level performance datasets introduction
MAC-level performance and parameters dataset for 802.15.4 wireless networks.

The *802.15.4-wireless-MAC-level-performance* datasets is a repository that stores measurements collected from the testbed facility about the MAC layer performance in IEEE 802.15.4 networks. The data is collected for my research on modeling the MAC-level performance in wireless sensor networks.
The data is also available for participants of the eWINE Grand Challenge: https://ewine-project.eu/grand-challenge/ .


**Experimental setup**.
To  understand  the  MAC-level packet delivery  performance several experiments in the wilab2 testbed have been set up.
We used 28 RM090 nodes with an IEEE 802.15.4 radio organized in a star-like network topology, as shown on the figure below. All nodes use a CSMA/CA MAC protocol and periodically generate a 100 B message to a single receiver located in the center of the topology. The transmission power  is  set  to  the  maximum, i.e. 5dBm,  to  ensure all nodes are in communication range.  To incorporate all factors that impact the MAC performance we setup several experiments varying the number of sending nodes (2-28 nodes), and the application traffic load (1pckt/2s, 1pckt/s, 2pckts/s, 4pckts/s, 8pckts/s, 16pckts/s and 64pckts/s).
We used a USRP B210 to generate controllable interference patterns by transmitting a modulated carrier for 2ms, followed by a 8ms idle period.

![experiment_setup](https://cloud.githubusercontent.com/assets/7999611/21597995/51e8ae4a-d154-11e6-8984-554d0109b8b1.png)

**Data collection**.
To simplify experiment control and data collection we created a global control program on the global controller using the Unified Programming Interfaces (UPIs) developed by the WiSHFUL project (http://www.wishful-project.eu/documents). We  run  several  experiments  with  the  aforementioned setups and measured several aspects of the MAC-level
performance, while the system was operating (around 21 hours).

For more details about the datasets please see the README file in the *datasets* folder. 

The *ML_model* folder contains the trained model from the publication in form of a Java binary serialized object exported from Weka.
