# WORK OF TRADUCHAT

Strumenti di lavoro per **TRADUCHAT** (traduchatchat.com · workoftraduchat.it).
L'app vera e propria è nel repository [UMBERTODECICCO75/traduchat](https://github.com/UMBERTODECICCO75/traduchat).

| Cartella | Contenuto |
|---|---|
| [`demo/`](demo/index.html) | Pagina demo "chiamate tradotte": simulazione con due telefoni, 3 scenari (Contatto, Fornitore, Assistenza) e 4 lingue, voce tradotta nel browser. Un solo file HTML, da caricare su qualsiasi hosting. |
| [`traduchat-twilio/`](traduchat-twilio/README.md) | Server Node.js per chiamate tradotte via Twilio (Voice SDK + ConversationRelay + DeepL), con pagina di test, componente React per Lovable e `setup-keliweb.sh` per installarlo sul VPS. |
| [`deploy/keliweb/setup-app.sh`](deploy/keliweb/setup-app.sh) | Installa o aggiorna l'app TraduChat (con sottotitoli tradotti nelle videochiamate) sul VPS Keliweb: build Node, pm2, nginx, HTTPS. |

## Installare l'app su Keliweb

```bash
git clone https://github.com/UMBERTODECICCO75/traduchat /opt/traduchat-app
sudo bash /opt/traduchat-app/deploy/keliweb/setup-app.sh app.workoftraduchat.it tua@email.it
```
Con un dominio principale (es. `workoftraduchat.it`) lo script configura anche `www`; con un sottodominio solo quello. Prima crea su Keliweb il record A che punta all'IP del VPS.

## Installare il server Twilio su Keliweb

```bash
git clone https://github.com/UMBERTODECICCO75/WORKOFTRADUCHAT- /opt/work-of-traduchat
cd /opt/work-of-traduchat/traduchat-twilio
sudo bash setup-keliweb.sh call.workoftraduchat.it tua@email.it
```
Dettagli e configurazione della Console Twilio in [`traduchat-twilio/README.md`](traduchat-twilio/README.md).
