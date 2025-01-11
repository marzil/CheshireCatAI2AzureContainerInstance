# Configurazione iniziale dell'ambiente

Ovviamente per poter iniziare dobbiamo avere un tenat di Azure con del credito attivo. Non disperate perche' Microsoft vi permette di avere 200€ di credito gratuito il primo mese per fare delle prove e poi le risorse che vengono utilizzate e che utilizzeremo durante questo esempio non hanno costi altissimi. Magari in un atro Markdown vi riporto i costi corretti ad oggi.

## Creiamo il Virtual Network

Prima operazione è quella di creare un Resource Group con il solo scopo di separare le risorse

![Create RG](../img/rg01.png)

Adesso creaimo la nostra Virtual Network.

![Create vn1](../img/vnet01.png)

Adesso scegliete il nome piu' adatto alla vostra vnet. Nel mio caso ho inserito vnetccaileonardo, ma voi sceglietene uno vostro.

![Choose name](../img/vnet02.png)

Infine scegliete la classe di indirizzi IP per agganciarvi. Mi raccomendo non scegliete una classe di IP in overlap con la vostra rete interna perchè nel caso deideriate agganciarvi tramite una VPN questo non permetterà di connettervi.

![Choose IP Address](../img/vnet03.png)

Adesso abilitate gli enpoint della vnet per lo storage account e gli altri servizi indispensabili.

![Enable endpoint](../img/vnet04.png)

Forse ne ho messo qualcuno in piu' del necessario, ma con calma potrete ridurli al necessario.

## Creiamo Open AI

Per or abbiamo creato OpenAI in francia perchè è li che abbiamo creato anche la vnet e desidero che il servizio di open ai non sia accessibile da qualsiasi parte ma solo dalle risorse all'interno della mia vnet.

Per cui selezioniamo il servizio Open AI

![Choose service](../img/OpenAI01.png)

A questo punto inseriamo il resource group corretto ed il nome per il nostro servizio.

![Define service](../img/OpenAI02.png)

Poi selezioniamo come accesso la Vnet corretta

![Define service](../img/OpenAI03.png)

Ed infine creiamo una distribuzione del nostro modello che poi ci servirà per configurare Cheshire Cat AI

![Define service](../img/OpenAI04.png)

Ed infine recuperiamo le chiavi per utilizzarle in Cheshire Cat AI

![Get Keys](../img/OpenAI05.png)

## Creaimo lo Storage Account

Ed ora finalmente poteremo lavorare per creare i volumi che ospiteranno i dischi di Docker. Cheshire cat ne utilizza 3 con scopi diversi e questo spazio ci servità per lavorare sui nostri ambienti

![Choose service](../img/storage01.png)

Dopo aver selezionato il servizio scegliete voi che tipo di ridondanza desiderate.

![Basic Configuration](../img/storage02.png)

Ed ora la rete, in modo tale che questo sia accessibile solo all'interno della vnet che abbiamo precedentemente creato.

![Storage vnet selection](../img/storage03.png)

Ed ora per verificare create pure una macchina virtuale all'interno della rete per vedere che a queste risorse potete accedere solo dall'interno della rete stessa.
