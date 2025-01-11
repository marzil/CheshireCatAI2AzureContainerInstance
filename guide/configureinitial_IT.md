# Configurazione iniziale dell'ambiente

Ovviamente per poter iniziare dobbiamo avere un tenat di Azure con del credito attivo. Non disperate perche' Microsoft vi permette di avere 200€ di credito gratuito il primo mese per fare delle prove e poi le risorse che vengono utilizzate e che utilizzeremo durante questo esempio non hanno costi altissimi. Magari in un atro Markdown vi riporto i costi corretti ad oggi.

## Creiamo il Virtual Network

Prima operazione è quella di creare un Resource Group con il solo scopo di separare le risorse

![Create RG](../img/rg01.png)

Adesso creaimo la nostra Virtual Network.

![Create vn1](../img/vnet01.png)

Adesso scegliete il nome piu' adatto alla vostra vnet. Nel mio caso ho inserito vnetccaileonardo, ma voi sceglietene uno vostro.

![Create vn1](../img/vnet02.png)

Infine scegliete la classe di indirizzi IP per agganciarvi. Mi raccomendo non scegliete una classe di IP in overlap con la vostra rete interna perchè nel caso deideriate agganciarvi tramite una VPN questo non permetterà di connettervi.

![Create vn1](../img/vnet03.png)

Adesso abilitate gli enpoint della vnet per lo storage account e gli altri servizi indispensabili.

![Create vn1](../img/vnet04.png)

Forse ne ho messo qualcuno in piu' del necessario, ma con calma potrete ridurli al necessario.

## Creiamo Open AI

## Creaimo lo Storage Account

