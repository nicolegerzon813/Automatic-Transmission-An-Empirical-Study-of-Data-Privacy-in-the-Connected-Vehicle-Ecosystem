# Automatic-Transmission-An-Empirical-Study-of-Data-Privacy-in-the-Connected-Vehicle-Ecosystem
Data and Paper for IMC publication

This repository provides the custom lists we made to classify different domains found in the vehicle and companion mobile app traffic. 

# ATA domain classification 
the file ```custom_list.txt``` describes the ATA domains and parent companies associated with those domains. 
Lines that begin with: 
* ! denote parent companies
* $ denote regex matched strings
* no preceeding symbol denotes a string matched directly 

# Integrated domain classification
the file ```integrated_third_parties.txt``` describes the integrated domains, purposes associated with those domains, and the vehicles/apps we observed having those integrations during our testing. 
Lines that begin with: 
* ! denote integrated third party purpose
* \# denote a list of vehicles and apps that integrate the domains into their core functionality 
* $ denote regex matched strings
* no preceeding symbol denotes a string matched directly 


# 1st party domains: 
Below is a list of the SLDs we consider first party for the apps as well as a conversion between app and vehicle. 

```
app_first_parties = {
    'Lucid' : ["atieva", "lucid", 'www.lucidmotors.com', 'lucidmotors.com', 'atieva.com', 'lucidcars.io'],
    'Lexus' : ["toyota.com", 'lexus.com', 'hir-multimedia.com'], 
    'Maserati' : ['maserati.com', 'fcagcv.com', 'fcagsdp.com'], 
    'RAM' : ['ramtrucks.com', 'fcagcv.com', 'www.ramtrucks.com', 'dodge.com', 'jeep.com', 'fiatusa.com', 'chrysler.com', 'fcagsdp.com'], 
    'Dodge' : ['dodge.com', 'fcagsdp.com'], 
    'MyNissan' : ['nissancloud.com', 'nissan-carwings.com', 'nssnfin.co', 'nissandime.com', 'nissanusa.com', 'heliosnissan.net', 'quick.guide'], 
    'Toyota' : ['toyota.com', 'toyotaaudioandconnectedservicessupport.com', 'hir-multimedia.com'],
    'FordPass' : ['ford.com', 'autonomic.ai'], 
    'MyCadillac' : ['gm.com', 'gm-cdn.com', 'gm.com:443', 'cadillac.com', 'chevrolet.com' , 'buick.com', 'onstar.com'], 
    'Volvo' : ['volvocars.com', 'volvo.care', 'volvocars.com:443', 'volvocars.biz'],
    'MySubaru' : ['subaru.com', 'connectedsubaru.io', 'subarucs.com', ], 
    'SubaruSolterra' : ['subaru.com', 'connectedsubaru.io', 'subarucs.com', 'toyota.com', 'hir-multimedia.com'], # toyota is on this list because it made the backend for the solterra and the solterra app
    'MyChevrolet' : ['gm.com', 'gm-cdn.com', 'gm.com:443', 'chevrolet.com', 'cadillac.com', 'onstar.com'],
    'MyChevroletBrian' : ['gm.com', 'gm-cdn.com', 'gm.com:443', 'chevrolet.com', 'cadillac.com', 'onstar.com'],
    'Rivian' : ['rivian.com', 'rivianservices.com'],
    'Tesla' : ['teslamotors.com', 'tesla.com', 'tesla.services'], 
    'LandRover' : ['jlrmotor.com', 'landrover.com', 'tata'], 
    'MercedesBenz' : ['mercedes-benz.com', 'corpinter.net'], 
    'Fisker' : ['fiskerinc.com'], 
    'myBuick' : ['gm.com', 'gm-cdn.com', 'gm.com:443', 'buick.com', 'cadillac.com', 'onstar.com'], 
    'myGMC' : ['gm-cdn.com',  'gmc.com', 'gm.com', 'cadillac.com', 'chevrolet.com', 'buick.com', 'onstar.com'], 
    'MyBMW' : ['bmwusa.com', 'bmwgroup.us','bmw.cloud', 'bmw.com', "bmwgroup.com"],
    'HondaLink' : ['honda.com', 'hondaweb.com', 'www.honda.com', 'gm.com'], # gm is on this list because the Honda Prologue was a partnership between GM and Honda›
    'Honda' : ['honda.com', 'hondaweb.com', 'www.honda.com'], 
    'Jeep' : ['jeep.com', 'www.jeep.com', 'ramtrucks.com', 'fiatusa.com', 'dodge.com', 'chrysler.com', 'fcagsdp.com'], 
    'KiaAccess' : ['kia.com', 'kiatechinfo.com'], 
    'MyVW' : ['ownersmanualvw.com', 'volkswagen.com'],
    'MINI' : ['mini.com', 'bmwusa.com', 'bmwgroup.com', 'miniusa.com', 'newcountrymini.com',],  
    'Lincoln' : ['ford.com', 'lincoln.com'],
    'Fiat' : ['fiat.com', 'fiatusa.com', 'fcagroup.com', 'jeep.com', 'dodge.com', 'ramtrucks.com', 'chrysler.com', 'fcagsdp.com'], 
    'GenesisIA' : ['hyundaiusa.com', 'genesis.com'], 
    'Chrysler' : ['chrysler.com', 'www.chrysler.com', 'jeep.com', 'ramtrucks.com', 'fiatusa.com', 'dodge.com', 'fcagsdp.com'], 
    'MyMazda' : ['mazda.com', 'mazdausa.com', 'mymazda.com',], 
    'MyHyundai' : ['hyundaiusa.com']
}
```

```

car_to_app = {
    'buick-envista' : "myBuick",
    'lucid-air' : "Lucid", 
    'lexus-nx450h' : 'Lexus', 
    'ram-bighorn' : 'RAM',
    'cadillac-lyriq' : 'MyCadillac',
    'chevrolet-blazer' : "MyChevrolet",
    'dodge' : 'Dodge',
    'fiat-500e' : 'Fiat',
    'fisker-ocean' : 'Fisker',
    'ford-f150' : 'FordPass',
    'ford-mustang' : 'FordPass',
    'honda-prologue' : 'HondaLink',
    'landrover-rangerover' : 'LandRover',
    'mercedes-eqs' : 'MercedesBenz',
    'nissan-ariya' : 'MyNissan',
    'rivian-R1S' : 'Rivian',
    'subaru-soltera' : 'SubaruSolterra',
    'tesla-model3' : 'Tesla',
    'tesla-cybertruck' : 'Tesla',
    'toyota-cross' : 'Toyota',
    'volvo-c40' : 'Volvo'
}

```
