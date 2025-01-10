<img src="https://i.giphy.com/media/v1.Y2lkPTc5MGI3NjExYXl1cDRjMW9wOWw3a3Vsa3plNGdjb2NraG5rajFxcTE3emZlNGpubyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/G0Odfjd78JTpu/giphy.gif">

Read Why Build an Automatic Watering System Part 1 [here](https://communicate.garden/2024/11/30/Why-build-an-automatic-irrigation-system-Part-1.html).

I was first inspired to build an automatic irrigation system by watching Grady Hillhouse's YouTube video, [Arduino Garden Controller - Automatic Watering and Data Logging](https://www.youtube.com/watch?v=O_Q1WKCtWiA). He concluded the video with the idea that the Arduino is one of many products marketed to "makers" and that these products are solutions looking for problems. Hillhouse's words resonate as I attempt to tackle the question, "Why build an automatic irrigation system?" for the second time. 

In my previous blog post, I pointed in many directions to define my problem. I offered that my plants were dying due to:

- the inefficient design of the watering can
- the fact that as a human I am undependable
- water scarcity 
- lack of metrics and accountability

November 26, 2024 I decided to improve overall as a gardener and start to log when I watered my plants and what phenomena I observed. The results are in the table below:

| Common Name   | Scientific Name | WaterLog1 (11/26-30/25) |  WaterLog 2 (12/17/25)| WaterLog3(12/28/24)| WaterLog4 (1/5/2025)|
| -------- | ------- | -------- | ------- | -------- | ------- | 
| Ghost Plant  | *Graptopetalum paraguayense*    | Indoors, 21 leaves, attracted cobwebs. | The top of the stem broke off. 16 leaves. |15 leaves. | 15 leaves. Looks droopy. Moved outside.|
| Black Prince | *Echeveria*     | Lost one of two plants. | 20 leaves. | Looks more green than purple.| No observable changes|
| Prickly Pear | *Opuntia ficus-indica* | Maybe suffering stem rot. Broke in half and has an exposed wound. Repotted today. Looks dead. |  
| Aloe vera | *Aloe vera*     | 30 plants, dehydrated. | Aloe in blue pot has no drainage and has gained a fly problem. | Looks vibrant. | No observable change. | 
| Split-leaf Philodendron | *Philodendron bipinnatifidum*     |  one green stem, short | 
| Rubber plant    | *Ficus elastica* | All leaves are curled inward, although not fallen off, and look recoverable with regular watering.  | Leaves unfurl. 11 leaves, 4 buds.| 13 leaves, 5 buds. | 21 leaves, 4 buds. I removed a few mealy bugs on young leaves.| 
| Corn plant    | *Dracaena fragrans* |Many leaves are damaged, likely by wind. Still continues to grow new leaves.  | 5 undamaged leaves total. Several dried and on yellowing.| Dried, dead leaves removed. Sprayed with neem oil. | 
| Swiss Cheese Plant |*Monstera deliciosa* | 4 leaves. One leaf is rotting with white fuzzy mealy bugs around its veins. | May need to remove leaf overcome by mealy bugs. | A new leaf is emerging. | New leaf fully emerged. Mealybugs are on all leaves, two must be cut. I used neem oil and a paper towel to wipe away the pest 3 leaves total.|
| Snake plant |*Sansevieria trifasciata* | 21.5 oz | Leaves look droopy and shriveled. It needs water to stand upright. | Looks more upright.| One leaf with mealybugs is yellowing at the tip. |
| ZZ plant |*Zamioculcas zamiifolia* | Lost a stem.  | Leaning towards the setting sun? | Maybe too windy. | Moved to an elevated position to not brush against the balcony fence.| 

I've taken responsibility for the intrinsically valuable lives of my plants and have noticed improvements in their health. I've learned that at a small scale, such as a balcony garden, human labor, time, and water aren't major costs. According to the 2023 [water rates](https://www.boardofwatersupply.com/bws/media/files/Honolulu-BWS-Rate-Handout_Feb2024_revAPR2024_1.pdf) provided by the Honolulu Board of Water Supply, the three gallons of tap water I give to the garden week costs about a cent. A professor of mine advised me to think of the persona of the person whose problem I'm trying to solve. If I were a farmer in Hawai'i, water would be one of the many costs of producing a crop. In addition to direct costs such as water, seeds, and fertilizer, there are operating (land costs, insurance, phone, marketing, transportation, etc) and capital costs (equipment, wash station, buildings, etc). [^1] 

This [map](https://geoportal.hawaii.gov/datasets/HiStateGIS::agricultural-land-use-2020-update/explore?location=21.532089%2C-158.037472%2C13.71) from the Hawaii Statewide GIS Program shows 2,745.55 acres of pineapples grown in Northshore O'ahu alongside Kamehameha highway. According to data from a nearby rain gauge, found on this [map](https://geoportal.hawaii.gov/datasets/ed0eca4ac4554febb86e0df2d30c59df_27/explore?location=21.474988%2C-158.059204%2C12.39), the area receives 1,062.38 mm of rainfall annually. 600 mm of rainfall a year is adequate for growing pineapples. In 2002, the College of Tropical Agriculture and Human Resources (CTHAR) at the University of Hawai'i - Manoa recommended drip irrigating pineapples with "47,000–94,000 liters of water per hectare per week" during periods of less rain. [^2] It could cost about $40-80K to water 2,745.55 acres of pineapples. Below is how attained that dollar value: 

>I used claude.ai to convert the units for CTHAR's recommended amount of water needed to irrigate >pineapples from liters per hectare to gallons per acre. 
>
>47,000 - 94,000 L/1 hectare /week --> 5, 025 - 10,051 gal/ acre/ week
>
>According to the Board of Water Supply's Agricultural Rates, each dwelling using 6,000 gal/month or more starting July 1, 2025, will be charged \\$2.81 per thousand gallons.
>
>Let's multiply the range by 4 to convert our units to gallons per acre per month. 
>
>20,100-40,204 gal/acre/month
>
>Now let's convert are units to every thousand gallons per acre per month, multiply by the rate, and >round to the nearest penny.. 
>
>20.1 kgal * 2.81 = \\$56.48
>40.204 kgal * 2.81 = \\$112.97
>
>This means it costs $56.48 - $112.97 to water an acre of pineapples for a month. 
>
>Let's multiply the range by our 2,745.55 acres of pineapples to get:
>
>\\$155,071.41 - \\$310,164.78
>
>Then divide the range by 4 to convert the units dollars per week.
>
>\\$38,767.85 - \\$77,541.20


According to Claude.ai, a pineapple farmer may harvest 15,000-20,000 pineapples per acre every 3-4 years. Pineapples cost about \\$6 at Amazon Whole Foods. Using those numbers, a 2,745.55-acre farm may generate \\$250 - \\$330 M in revenue. Using the dollar range I calculated for water cost per week, I estimate it could cost \\$6 - \\$16 M to water one's pineapple farm until the first harvest assuming the farm was irrigated year-round.

I believe our problem is that we must simulate perfect weather conditions without a true ability to control the weather for optimal plant growth. A traditional drip irrigation system runs on a schedule whereas an automatic irrigation system is soil moisture sensor-based. Given that rainfall varies throughout the year, there is an opportunity to save on water from the Board of Water Supply System, by having irrigation systems able to turn off when detecting rainfall. An automatic irrigation system still may be too expensive to justify the savings in water use.

It may be easier to justify using an automatic irrigation system to grow food on a submarine or spaceship, where freshwater is irrefutably scarce and the budgets are bigger. I'm building an automatic irrigation system for one of my plants in the garden to learn electrical engineering, programming, and networking skills. Since I am not selling my plants and increases in efficiency would save me only pennies rather than millions, the thing of value I am producing is probably knowledge. I don't have a green house or acre of land to further agricultral science, but using technology to turn my balcony into a more controlled environment will help me obtainer cleaner data to answer scientific questions. 

[^1]: “How Much Does It Cost to Grow or Produce Your Product? - Gofarm Hawaii.” GoFarm Hawaii - GoFarm Hawaii, The University of Hawaii, 18 Oct. 2018, gofarmhawaii.org/how-much-does-it-cost-to-grow-or-produce-your-product/. 

[^2]: Bartholomew, Duane P, et al. “Pineapple Cultivation in Hawaii.” CTAHR, University of Hawaii Cooperative Extension Service , Oct. 2002, www.ctahr.hawaii.edu/oc/freepubs/pdf/f_n-7.pdf. 


. 
