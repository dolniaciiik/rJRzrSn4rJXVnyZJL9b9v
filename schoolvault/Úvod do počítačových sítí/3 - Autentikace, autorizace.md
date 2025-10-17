**Autentikace** = proces ověření identity 
**Autorizace** = vymezení rozsahu služeb

Lokální prostředky autentikace:
* znalost (heslo, pin)
* technické prostředky
* biometrie
Vzdálené:
* ochrana proti odposlechu: jednorázová hesla OTP, kryptografie
* přenos dat v protokolu: např. SASL (protokoly na základě *profilů*)
* použití autentikačního serveru a protokolu (LDAP, RADIUS,...)

### OTP 
* pův. varianta -> vytištěný seznam otp
* *challange-response* -> server vyšle náhodný kód, klient vyrobí odpověd a pošle ji serveru
* moderně -> uživatel dostane token, který generuje jednorázový časově omezený kód

### Kryptografie
* historicky -> šifrovací mřížky
* současnost -> analogické principy v digitální podobě 

### Asymetrická kryptografie
* použití páru neodvoditelných klíčů
* matem. základ -> jednocestné funkce
	* násobení X rozklad prvočísel
	* m=p^k mod q
* např. RSA, DSA, ECDSA
* výhody: odpadá problém sdíleného tajemství

### Hashovací funkce
-> vytvoří pevný kód z daného textu
-> např. CRC, MD5

pro kryptografii:
* jednocestnost 
* nalezení shodného textu je skoro nemožné
* např. SHA

### Diffie-Hellmanův algoritmus
* postup:
	1.  alice generuje random a a veřejná p,q
	2.  spočítá A = p^a mod q  a pošle p,q a A bobovi
	3.  Bob zvolí tajné b, spočte B = p^b mod q a pošle B alici

### Certifikáty
* self-signed certificate - na konci retezce autorit nekonci nijak rozumne
* struktura podle X.509