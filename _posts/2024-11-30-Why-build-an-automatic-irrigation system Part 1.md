![Image of pitcher watering ZZ plant](/assets/water.gif)


My plants need more attention. Inspired by [Grady Hillhouse](https://www.youtube.com/watch?v=O_Q1WKCtWiA),  I have challenged myself to build an automatic irrigation system.

 The first step of the [engineering design process](https://www.youtube.com/watch?v=MFGg1calQ6k) is problem definition. Before jumping into the fun of building an automatic irrigation system for my garden, we must understand what problem we're addressing. This prevents wasted time, energy, and resources. 

I manually irrigate my garden using a 2-gallon watering can. Using a watering can to irrigate plants may lead to waste or underwatering. Watering cans dispense imprecise amounts of water and plants have specific requirements for water. The following is a table outlining the volume of water and frequency of watering each of my plants needs. These values were calculated using the plant identifier app, [PictureThis](https://www.picturethisai.com), along with additional data such as plant container size and estimations of sun exposure.

| Common Name   | Scientific Name | Volume of Water Required |  Irrigation Frequency|
| -------- | ------- | -------- | ------- |
| Ghost Plant  | *Graptopetalum paraguayense*    | 1 oz | Every 2 weeks |
| Black Prince | *Echeveria*     | 3.2 oz | Every week |
| Prickly Pear | *Opuntia ficus-indica* | 10.8 oz | Every week |
| Aloe vera | *Aloe vera*     | 9 oz | Every week |
| Split-leaf Philodendron | *Philodendron bipinnatifidum*     | 25.2 oz | 2-3 times a week |
| Rubber plant    | *Ficus elastica* | 21.5 oz | 2-3 times a week |
| Corn plant    | *Dracaena fragrans* |21.5 oz | Every week |
| Swiss Cheese Plant |*Monstera deliciosa* | 80.9 oz | 2-3 times a week |
| Snake plant |*Sansevieria trifasciata* | 21.5 oz | Every week |
| ZZ plant |*Zamioculcas zamiifolia* | 14.5 oz | Every 2 weeks |

Since I cannot dispense exact amounts of water from a watering can, I will likely over or underwater my plants leading to poor plant health and an inefficient use of resources. 

When and how much I should irrigate are often arbitrary decisions rather than information-based. My ability to evaluate the conditions of my plants is limited. There are visual indicators of plant stress such as yellowing leaves, but these signs can be confused with signs of disease. I may also use my sense of touch to feel whether the soil is moist or not, but my observations don't compare to those of a soil sensor.  Despite the option to use information gathered from observation to decide when and how much I should water my garden, the irrigation schedule is generally based on my mood. My plants have just suffered weeks without water due to my bad habits and lack of empathy. Watering plants based on how I feel and my observations have led to poor plant health. 

Freshwater is a scarce, shared resource. The global water supply falls short of water demand. According to a 2021 report titled, "Water Conflicts: From Ancient to Modern Times and in the Future" [^1],  the amount of water that is today economically available for human use for all uses is about 4600 km^3/yr...Total water demand is expected to increase from 4600 today to 5500 km^3/yr in 2050". For context, the Earth has millions of cubic kilometers of freshwater, which may be found in glaciers, the ground, the atmosphere, lakes, and rivers. Rivers are a more accessible source of freshwater to humans than other sources, but rivers only account for 2,120 km^3 or 1/10,000th of one percent of the total water on Earth. [^2] Water scarcity is further complicated by the fact that many water systems worldwide are transboundary (e.g., rivers, lakes, and groundwater aquifers). The "Water Conflicts" report explains, "Such transboundary or cross-border water systems can always be a cause for competition among the countries that share them. This is reflected in the English language, as the word rival, which has the meaning, “I am competing”, has its root in the Latin word rivalis, which means sharing the same river with someone else.

In Hawaiʻi, the 2 primary issues with water issues are its scarcity and the pollution of surface water linked to both agricultural and non-agricultural activities.[^3] According to the [Board of Water Supply for Honolulu](https://www.boardofwatersupply.com/water-resources/oahu-water-history), the island experienced a water boom in the 1800s when plantation owners and ranchers quickly depleted the water supply by digging wells. Recent events such as the leakage of fuel from the Red Hill Underground Fuel Storage Facility into the freshwater aquifer beneath the island of Oahu, Hawaiʻi have increased sensitivity to these issues, with specific concerns for public health. Tensions around sharing the little amount of water we have have existed before and exist now. 

Measuring water usage supports accountability in water governance processes.  Currently, when and how much my plants get watered is information loosely held in my memory. My evidence for responsible water use is weak and anecdotal. This is also a problem at scale. In a paper presenting the World Bank's water strategy, the author, Pieter Waalewijn [^4], expresses that the agricultural sector as well as the irrigation and drainage sector need to improve their "metrics of success" and create "stronger accountability on actual service delivery". Supporting this idea of better data on water usage leading to an ability to hold farmers and others accountable, a paper overviewing smart irrigation systems using IoT devices [^5], refers to the United Nations Sustainable Development goal, 6.4, which deals with water scarcity. The two main indicators for water scarcity are water use eﬃciency and water stress. The authors write, "The quality of the assessment of [these indicators] depends primarily on the quality of available water data."

Globally and in my garden, how we should control our water usage should be based on quality water data. For this blog, the technology I'm using to irrigate is imprecise and potentially wasteful, my irrigation scheldule is random, my plants require different amounts of water at different times, and there is no system in place to evaluate in real-time how much water is used to support better water governance. The purpose of this blog post was to think about my garden's need for water while relating to the problem of global and regional agricultural needs for water. 


[^1]: Angelakis,A.N.;Valipour, M.; Ahmed, A.T.; Tzanakakis, V.; Paranychianakis, N.V.; Krasilnikoff, J.; Drusiani, R.; Mays, L.; El Gohary, F.; Koutsoyiannis, D.; et al. Water Conflicts: From Ancient to Modern Times and in the Future. Sustainability 2021,13,4237. https://doi.org/ 10.3390/su13084237
[^2]: Water Science School. “How Much Water Is There on Earth?” How Much Water Is There on Earth?, U.S. Geological Survey, U.S. Geological Survey, 13 Nov. 2019, www.usgs.gov/special-topics/water-science-school/science/how-much-water-there-earth. 
[^3]: Chhimcanal, Bunneam. “Farming Practices and Implications for Water Quality and Sustainability on Oʻahu, Hawaiʻi.” University of Hawaiʻi at Mānoa, 2024. 
[^4]: Waalewijn, Pieter. “ Reformulating the value proposition of water in agriculture under changing conditions.” Irrigation and Drainage , Jan. 2021, https://doi.org/10.1002/ird.2569. 
[^5]: Obaideen, Khaled, et al. “An overview of smart irrigation systems using IOT.” Energy Nexus, vol. 7, Sept. 2022, p. 100124, https://doi.org/10.1016/j.nexus.2022.100124.
