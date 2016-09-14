# KepoRemoteControl
Ideja je da se ostvari komunikacija između mikrokontrolera (arduino) sa jedne strane, i kotla odnosno njegovog fabričkog mikrokontrolera sa druge strane, a sve u cilju praćenja vitalnih parametara u toku rada kao i zbog samog upravljanja kotlom (paljenje, gašenje, regulacija temperature itd...). Nekoliko domaćih proizvođača kotlova na pelet koriste istu platformu, tako da se koncept može primeniti ne samo na "Kepo" kotlove, nego i na kotlove "Milan Blagojević Smederevo" i "Alfa Plam Vranje".

U samom kotlu je ugrađena upravljačka ploča italijanskog proizvođača Micronova (model i023). Na njoj se nalazi konektor CN13 koji je namenjen za povezivanje servisnog instrumenta koji se koristi za očitavanje i upisivanje parametara rada kotla. Zamisao je da arduino simulira rad ovog servisnog instrumenta, pa da se na taj način očitavaju i upisuju željeni parametri rada. Glavna ploča "priča" sa instrumentom posredstvom serijske komunikacije (baud rate 1200, 8 data bits, 2 stop bits, no parity, no flow control) s tim da je tip realizacije half-duplex što znači da se ista žica koristi i za slanje i za primanje (TxRx)


