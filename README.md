# APRIORI-ALG-DA

Gjetja e Bashkësive të Shpeshta:

Fillimisht, identifikohen të gjitha bashkësitë e artikujve që kanë një mbështetje (support) të lartë, ku mbështetja është numri i transaksioneve që përmbajnë bashkësinë.
Këto bashkësi të shpeshta përdoren për të gjeneruar bashkësi më të mëdha që gjithashtu kanë mbështetje të lartë.
Gjenerimi i Rregullave të Shoqërimit:

Nga bashkësitë e shpeshta, gjenerohen rregullat e shoqërimit që plotësojnë një prag të caktuar për besueshmërinë (confidence), ku besueshmëria është probabiliteti që një bashkësi artikujsh të përmbajë një artikull të caktuar.
Formula për Mbështetjen dhe Besueshmërinë
Mbështetja (Support): Mbështetja e një bashkësie artikujsh 
X
X është përqindja e transaksioneve që përmbajnë 
X
X.
Support
(
X
)
=
Numri i transaksioneve q
e
¨
 p
e
¨
rmbajn
e
¨
 
X
Numri total i transaksioneve
Support(X)= 
Numri total i transaksioneve
Numri i transaksioneve q 
e
¨
  p 
e
¨
 rmbajn 
e
¨
  X
​
 

Besueshmëria (Confidence): Besueshmëria e një rregulli 
X
→
Y
X→Y është përqindja e transaksioneve që përmbajnë 
Y
Y duke pasur parasysh që ato përmbajnë 
X
X.
Confidence
(
X
→
Y
)
=
Support
(
X
∪
Y
)
Support
(
X
)
Confidence(X→Y)= 
Support(X)
Support(X∪Y)
​
 

Shembull
Në një dyqan, nëse shumë klientë që blejnë qumësht gjithashtu blejnë bukë, algoritmi Apriori mund të identifikojë këtë lidhje dhe të gjenerojë një rregull të shoqërimit si 
qum
e
¨
sht
→
buk
e
¨
qum 
e
¨
 sht→buk 
e
¨
 .

Hapi 1: Gjetja e Bashkësive të Shpeshta
Supozojmë se kemi këto transaksione:

T1: {qumësht, bukë, vezë}
T2: {qumësht, bukë}
T3: {bukë, birrë}
T4: {qumësht, bukë, birrë}
T5: {bukë, vezë}
Copy
Me pragun e mbështetjes 60% (3 nga 5 transaksione):

Bashkësitë e shpeshta janë: {qumësht, bukë}, {bukë, vezë}, {bukë, birrë}
Hapi 2: Gjenerimi i Rregullave të Shoqërimit
Nga bashkësitë e shpeshta, gjenerojmë rregullat:

qum
e
¨
sht
→
buk
e
¨
qum 
e
¨
 sht→buk 
e
¨
 
buk
e
¨
→
veze
buk 
e
¨
 →veze
buk
e
¨
→
birr
e
¨
buk 
e
¨
 →birr 
e
¨
 
Llogaritja e besueshmërisë:

Confidence
(
qum
e
¨
sht
→
buk
e
¨
)
=
Support
(
qum
e
¨
sht
∪
buk
e
¨
)
Support
(
qum
e
¨
sht
)
Confidence(qum 
e
¨
 sht→buk 
e
¨
 )= 
Support(qum 
e
¨
 sht)
Support(qum 
e
¨
 sht∪buk 
e
¨
 )
​
 
