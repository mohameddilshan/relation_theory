# relation_theory
#Sep 18,2023
---
##Relation 1

|**Driver ID**|**Driver Name**|**Bus Number**|
|---          |---            |---           |
|001          |"Harry"        |8877          |
|002          |"Ron"          |4940          |
|003          |"Hermoine"     |4550          |
|004          |"Remus"        |4546          |

##Relation 2

|**conductor id**|**conductor**|**Bus Number**|
|---             |---          |---           |
|010             |"Tokyo"      |3281          |
|011             |""nairobi""    |4550        |
|012             |"Reo"        |4667          |
|013             |"Berlin"     |8877          |

##find the relation of Dare the driver and conductor traveling in a bus?

###projuction
Relation1,Driver Name,Bus Number
|**Driver Name**|**Bus Number**|
|---            |---           |
|"Harry"        |8877          |
|"Ron"          |4940          |
|"Hermoine"     |4550          |
|"Remus"        |4546          |

Relation2,Conductor name,bus number
|**conductor**|**Bus Number**|
|---          |---           |
|tokyo        |3281          |
|"nairobi"      |4550          |
|"Reo"        |4667          |
|"Berlin"     |8877          |





###cross product
Relation1XRelation2
|**Driver Name**|**Bus Number**|**conductor**|**Bus Number**|
|---            |---           |---          |---           |
|"Harry"        |8877          |tokyo        |3281          |
|"Harry"        |8877          |"nairobi"      |4550          |
|"Harry"        |8877          |"Reo"        |4667          |
|"Harry"        |8877          |"Berlin"     |8877          |
|"Ron"          |4940          |tokyo        |3281          |
|"Ron"          |4940          |"nairobi"      |4550          |
|"Ron"          |4940          |"Reo"        |4667          |
|"Ron"          |4940          |"Berlin"     |8877          |
|"Hermoine"     |4550          |tokyo        |3281          |
|"Hermoine"     |4550          |"nairobi"      |4550          |
|"Hermoine"     |4550          |"Reo"        |4667          |
|"Hermoine"     |4550          |"Berlin"     |8877          |
|"Remus"        |4546          |tokyo        |3281          |
|"Remus"        |4546          |"nairobi"      |4550          |
|"Remus"        |4546          |"Reo"        |4667          | 
|"Remus"        |4546          |"Berlin"     |8877          |

###filter
Relation1.Bus Number = Relation2.Bus Number
|**Driver Name**|**Bus Number**|**conductor Name**|**Bus Number**|
|---            |---           |---               |---           |
|"Harry"        |8877          |"Berlin"          |8877          |
|"Hermoine"     |4550          |"nairobi"           |4550          |

###projuction
Relation1.Driver name,Relation2.Conductor Name

|"Harry"   |"Berlin"|
|"Hermoine"|"nairobi" |

##which conductor work with driver "Harry"?

###projuction
Relation1.Driver Name

|**Driver Name**  |
|---              |
|"Harry"          |
|"Ron"            |
|"Hermoine"       |
|"Remus"          |

Relation2.condoctur Name

|**conductor Name**|
|---               |
|Tokyo             |
|"nairobi"           |
|"Reo"             |
|"Berlin"          |

###Cross Product
Relation1XRelation2
|**Driver Name**|**conductor Name**|
|---            |---               |
|"Harry"        |Tokyo             |
|"Harry"        |"nairobi"           |
|"Harry"        |"Reo"             |
|"Harry"        |"Berlin"          |
|"Ron"          |Tokyo             |
|"Ron"          |"nairobi"           |
|"Ron"          |"Reo"             |
|"Ron"          |"Berlin"          |
|"Hermoine"     |Tokyo             |
|"Hermoine"     |"nairobi"           |
|"Hermoine"     |"Reo"             |
|"Hermoine"     |"Berlin"          |
|"Remus"        |Tokyo             |
|"Remus"        |"nairobi"           |
|"Remus"        |"Reo"             |
|"Remus"        |"Berlin"          |

###Filter 
Relation1.Driver Name = "Harry"

|**Driver Name**  |**conductor Name**|
|---              |---               |
|"Harry"          |Tokyo             |
|"Harry"          |"nairobi"           |
|"Harry"          |"Reo"             |
|"Harry"          |"Berlin"          |

###Projuction
Relation2.condutor Name
|Tokyo  |
|"nairobi"|
|Reo    |
|Berlin |
