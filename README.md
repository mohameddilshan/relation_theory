#relation_theory
#Sep 18,2023
---
##Relation 1
|**Driver ID**|**Driver Name**         |**Bus Number**         |
|---          |---                     |---                    |
|001(D.I, INT)|"harry"(D.N,STR)        |8877(B.N,INT)          |
|002(D.I, INT)|"Ron"(D.N,STR)          |4940(B.N,INT)          |
|003(D.I, INT)|"Hermoine"(D.N,STR)     |4550(B.N,INT)          |
|004(D.I, INT)|"Remus"(D.N,STR)        |4546(B.N,INT)          |

##Relation 2
|**conductor id**|**conductor**|**Bus Number**|
|---             |---          |---           |
|010(C.I,INT)    |"tokyo(C,N,STR)"      |3281(B.N1,INT)|
|011(C.I,INT)    |"nairobi(C,N,STR)"    |4550(B.N1,INT)|
|012(C.I,INT)    |"reo(C,N,STR)"        |4667(B.N1,INT)|
|013(C.I,INT)    |"berlin(C.N,STR)"     |8877(B.N1,INT)|

##Find the conductor and the bus driver working in the same bus?

###Projection
Relation1,Driver Name,Bus Number
|**Driver Name**         |**Bus Number**|
|---                     |---           |
|"harry"(D.N,STR)        |8877(B.N,INT) |
|"Ron"(D.N,STR)          |4940(B.N,INT) |
|"Hermoine"(D.N,STR)     |4550(B.N,INT) |
|"Remus"(D.N,STR)        |4546(B.N,INT) |

Relation2,Conductor name,bus number
|**conductor**         |**Bus Number**          |
|---                   |---                     |
|tokyo(C,N,STR)        |3281(B.N1,INT)          |
|"nairobi(C,N,STR)"    |4550(B.N1,INT)          |
|"reo(C.N,STR)"        |4667(B.N1,INT)          |
|"berlin(C.N,STR)"     |8877(B.N1,INT)          |





###cross product
Relation1XRelation2
|**Driver Name**|**Bus Number**|**conductor**|**Bus Number**|
|---            |---           |---          |---           |
|"harry"(D.N,STR)        |8877(B.N,INT)          |tokyo(C,N,STR)        |3281(B.N1,INT)          |
|"harry"(D.N,STR)        |8877(B.N,INT)          |"nairobi(C,N,STR)"      |4550(B.N,INT)          |
|"harry"(D.N,STR)        |8877(B.N,INT)          |"reo(C,N,STR)"        |4667(B.N1,INT)          |
|"harry"(D.N,STR)        |8877(B.N,INT)          |"berlin(C.N,STR)"     |8877(B.N,INT)          |
|"Ron"(D.N,STR)          |4940(B.N,INT)          |tokyo(C,N,STR)        |3281(B.N1,INT)          |
|"Ron"(D.N,STR)          |4940(B.N,INT)          |"nairobi(C,N,STR)"      |4550(B.N,INT)          |
|"Ron"(D.N,STR)          |4940(B.N,INT)          |"reo(C,N,STR)"        |4667(B.N1,INT)          |
|"Ron"(D.N,STR)          |4940(B.N,INT)          |"berlin(C.N,STR)"     |8877(B.N,INT)          |
|"Hermoine"(D.N,STR)     |4550(B.N,INT)          |tokyo(C,N,STR)        |3281(B.N1,INT)          |
|"Hermoine"(D.N,STR)     |4550(B.N,INT)          |"nairobi(C,N,STR)"      |4550(B.N,INT)          |
|"Hermoine"(D.N,STR)     |4550(B.N,INT)          |"reo(C,N,STR)"        |4667(B.N1,INT)          |
|"Hermoine"(D.N,STR)     |4550(B.N,INT)          |"berlin(C.N,STR)"     |8877(B.N,INT)          |
|"Remus"(D.N,STR)        |4546(B.N,INT)          |tokyo(C,N,STR)        |3281(B.N1,INT)          |
|"Remus"(D.N,STR)        |4546(B.N,INT)          |"nairobi(C,N,STR)"      |4550(B.N,INT)          |
|"Remus"(D.N,STR)        |4546(B.N,INT)          |"reo(C,N,STR)"        |4667(B.N1,INT)          | 
|"Remus"(D.N,STR)        |4546(B.N,INT)          |"berlin(C.N,STR)"     |8877(B.N,INT)          |

###filter
Relation1.Bus Number = Relation2.Bus Number
|**Driver Name**|**Bus Number**|**conductor Name**|**Bus Number**|
|---            |---           |---               |---           |
|"harry"(D.N,STR)        |8877(B.N,INT)          |"berlin(C.N,STR)"          |8877(B.N,INT)          |
|"Hermoine"(D.N,STR)     |4550(B.N,INT)          |"nairobi(C,N,STR)"           |4550(B.N,INT)          |

###Projection
Relation1.Driver name,Relation2.Conductor Name

|"harry"(D.N,STR)   |"berlin(C.N,STR)"|
|"Hermoine"(D.N,STR)|"nairobi(C,N,STR)" |

##which conductor work with driver "harry"(D.N,STR)?

###Projection
Relation1.Driver Name

|**Driver Name**  |
|---              |
|"harry"(D.N,STR)          |
|"Ron"(D.N,STR)            |
|"Hermoine"(D.N,STR)       |
|"Remus"(D.N,STR)          |

Relation2.condoctur Name

|**conductor Name**|
|---               |
|tokyo(C,N,STR)             |
|"nairobi(C,N,STR)"         |
|"reo(C,N,STR)"             |
|"berlin(C.N,STR)"          |

###Cross Product
Relation1XRelation2
|**Driver Name**|**conductor Name**|
|---            |---               |
|"harry"(D.N,STR)        |tokyo(C,N,STR)             |
|"harry"(D.N,STR)        |"nairobi(C.N,STR)"         |
|"harry"(D.N,STR)        |"reo(C,N,STR)"             |
|"harry"(D.N,STR)        |"berlin(C.N,STR)"          |
|"Ron"(D.N,STR)          |tokyo(C,N,STR)             |
|"Ron"(D.N,STR)          |"nairobi(C,N,STR)"         |
|"Ron"(D.N,STR)          |"reo(C,N,STR)"             |
|"Ron"(D.N,STR)          |"berlin(C.N,STR)"          |
|"Hermoine"(D.N,STR)     |tokyo(C,N,STR)             |
|"Hermoine"(D.N,STR)     |"nairobi(C,N,STR)"         |
|"Hermoine"(D.N,STR)     |"reo(C,N,STR)"             |
|"Hermoine"(D.N,STR)     |"berlin(C.N,STR)"          |
|"Remus"(D.N,STR)        |tokyo(C,N,STR)             |
|"Remus"(D.N,STR)        |"nairobi(C,N,STR)"         |
|"Remus"(D.N,STR)        |"reo(C,N,STR)"             |
|"Remus"(D.N,STR)        |"berlin(C.N,STR)"          |

###Filter 
Relation1.Driver Name = "harry"(D.N,STR)

|**Driver Name**  |**conductor Name**|
|---              |---               |
|"harry"(D.N,STR)          |tokyo(C,N,STR)             |
|"harry"(D.N,STR)          |"nairobi(C,N,STR)"         |
|"harry"(D.N,STR)          |"reo(C,N,STR)"             |
|"harry"(D.N,STR)          |"berlin(C.N,STR)"          |

###Projection
Relation2.condutor Name
|tokyo(C,N,STR)  |
|"nairobi(C,N,STR)"|
|reo(C,N,STR)    |
|berlin(C.N,STR) |
