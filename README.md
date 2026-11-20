# All-in-One Histeon Traghetto (aiohtraghetto)

Un programma per Linux (AppImage) e un plugin per WordPress che portano **All-in-One WP Migration** sul computer: backup e ripristini senza limiti di dimensione, più destinazioni e archivi cloud, backup programmati, reti multisito (la rete intera o un sito alla volta, e un sito rimesso al suo posto nella rete) e una pagina «Backup» nella bacheca della rete che funziona anche senza l'estensione Multisite. Fa parte della famiglia di Histeon.

Questo repository pubblica soltanto le **release firmate**; lo sviluppo avviene altrove.

## Release firmate

Ogni release ha:

- `aiohtraghetto-X.Y.Z-x86_64.AppImage`, il programma, con `aiohtraghetto-X.Y.Z-x86_64.AppImage.minisig`;
- `aiohtraghetto-X.Y.Z.zip`, il plugin per WordPress, con `aiohtraghetto-X.Y.Z.zip.minisig`.

Il plugin si aggiorna da sé dall'amministrazione di WordPress (anche con MainWP): prima di installare scarica ZIP e firma e li controlla con la chiave di rilascio, e un pacchetto senza firma valida non viene mai installato. Nessun dato del sito viene inviato. `AIOHTRAGHETTO_UPDATES` a `false` in `wp-config.php` spegne gli aggiornamenti.

Il programma controlla all'avvio se c'è una versione nuova e, con un clic, la scarica, ne verifica la firma e sostituisce l'AppImage. `AIOHTRAGHETTO_AGGIORNAMENTI=0` spegne il controllo.

Chiave pubblica di rilascio (id `7245FEACC0E94D12`):

```
RWQSTenArP5FclHgI0qEErGDYUEQ6gL4cEhpgec49VKtqKfgl2TIAn5W
```

Per verificare a mano: `minisign -Vm aiohtraghetto-X.Y.Z.zip -P RWQSTenArP5FclHgI0qEErGDYUEQ6gL4cEhpgec49VKtqKfgl2TIAn5W`.

## Privacy

Come il programma usa Google Drive e quali dati tocca: [PRIVACY.md](PRIVACY.md).

## Licenza e marchi

Il plugin è GPL-3.0-or-later: il testo è in [LICENSE.txt](LICENSE.txt).

Non è affiliato a ServMask. «All-in-One WP Migration» è un marchio del suo titolare ed è nominato solo per dire con che cosa è compatibile: vedi [TRADEMARKS.md](TRADEMARKS.md).
