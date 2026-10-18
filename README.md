# raspberry
# Laboratorio di Sistemi e Reti con Raspberry Pi 3B

Piano annuale semplificato per le classi 3^ e 5^ ITIS Informatico. Il Raspberry Pi 3B funge da server centrale per i test pratici e l'uso della riga di comando.

---

## 🛠️ Setup Essenziale (Lato Docente)

**1. Accesso Remoto Semplificato**
Evita configurazioni complesse sul router della scuola: installa **Tailscale** sul Raspberry Pi. Fornirà un IP fisso raggiungibile da qualsiasi PC (dove i ragazzi installeranno il client Tailscale o useranno una web-GUI).

**2. Creazione Account e Controllo**
Crea gli utenti in blocco e forza il salvataggio dei comandi con data e ora per poterli controllare.
*Script di creazione rapida:*
```bash
for i in {01..25}; do sudo useradd -m -s /bin/bash studente$i && echo "studente$i:Cambiami$i" | sudo chpasswd; done
