# SAM-Audio App - Product Requirements Document

## 1. Panoramica del Prodotto

### Scopo
Interfaccia semplice e intuitiva per utilizzare il modello SAM-Audio di Meta per la separazione di sorgenti audio, specificamente ottimizzata per il lavoro di coreografia e produzione di spettacoli di pattinaggio.

### Obiettivo Primario
Permettere l'isolamento e l'estrazione di elementi audio specifici (voce, strumenti, suoni ambientali) da mix complessi in modo completamente gratuito, illimitato e senza vincoli.

---

## 2. Casi d'Uso Principali

### Per Coreografi e Produttori
- **Isolare la voce** da una traccia musicale per creare versioni strumentali
- **Estrarre singoli strumenti** (batteria, basso, piano) per remix creativi
- **Separare dialoghi/annunci** da musica di sottofondo
- **Pulire registrazioni live** rimuovendo rumori indesiderati
- **Creare stem separati** per editing audio avanzato
- **Sincronizzare audio con video** di performance (prompting visivo)

---

## 3. Architettura Tecnica Raccomandata

### Soluzione: **App Desktop Locale + Web Interface**

#### Perché questa scelta?
✅ **Completamente gratuito** dopo il setup iniziale
✅ **Illimitato** - nessun costo per elaborazione
✅ **Privacy totale** - file audio restano sul tuo computer
✅ **Performance ottimali** - sfrutta GPU locale
✅ **Nessun abbonamento cloud** - zero costi ricorrenti

#### Stack Tecnologico

**Frontend:**
- **Gradio** (interfaccia web automatica in Python)
  - Generazione UI automatica
  - Mobile-responsive di default
  - Zero configurazione frontend
  - Accessibile via browser locale

**Backend:**
- **Python 3.10+** con SAM-Audio
- **PyTorch** con CUDA per GPU NVIDIA
- **FastAPI** (opzionale, se serve più personalizzazione)

**Deployment:**
- Localhost (http://localhost:7860)
- Opzionale: Tunneling con ngrok/Cloudflare Tunnel per accesso remoto

---

## 4. Requisiti di Sistema

### Minimi
- **GPU:** NVIDIA con almeno 8GB VRAM (RTX 3060 o superiore)
- **RAM:** 16GB
- **Storage:** 10GB liberi (per modelli)
- **OS:** Windows 10/11, Linux (Ubuntu 20.04+)
- **Python:** 3.10 o superiore

### Raccomandati
- **GPU:** NVIDIA RTX 4070 o superiore (12GB+ VRAM)
- **RAM:** 32GB
- **Storage:** SSD con 20GB liberi

---

## 5. Interfaccia Utente - Design

### Layout Principale (Interfaccia Gradio)

