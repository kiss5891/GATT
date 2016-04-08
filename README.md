# GATT
## BLE 低功耗藍牙
![BLE](/image/BLE-training.jpg)

##ATT與GATT
###ATT(Attribute Protocol)
所有數據傳輸經過這層實現(ATT)，定義了Client和Server，Client就傳Request，Server傳response。
###GATT(Generic Attribute Profile)
具體實現數據的傳輸(GATT)。 Server上所有的ATT成為一個一個的。   
Services，通過這樣的形式把數據包給Client。把ATT定義的屬性根據不同的服務進行 歸類、組合，同時把一系列的讀寫整合起來，成為一系列的數據通信操作流程，提供給上層的Profile去用。
##ATT
存資料的資料結構   
三種元素   
- 一個16位的handle   
- 一個UUID，定義了attribute的類型   
- 一個value

##GATT protocol
![GATT protocol](/image/GATT profiles.png)
###Service (服務)
每個Service裡，會包含多個Characteristics
###Characteristics (特徵)
每個Characteristics會有一個property(屬性)、value(值)以及數個descriptor(描述)

