# 🚀 SAM-Audio Studio - Guida Rapida

## Come Iniziare in 5 Minuti

### Passo 1: Apri il Notebook su Google Colab

1. **Carica il file** `SAM_Audio_Studio.ipynb` su Google Colab:
   - Vai su [Google Colab](https://colab.research.google.com)
   - Clicca su **File → Carica notebook**
   - Seleziona `SAM_Audio_Studio.ipynb` dal tuo computer

   **Oppure:**
   - Salva il file su Google Drive
   - Da Google Drive: click destro → Apri con → Google Colaboratory

### Passo 2: Attiva la GPU

⚠️ **IMPORTANTE:** SAM-Audio richiede una GPU per funzionare

1. Nel menu di Colab: **Runtime → Change runtime type**
2. Seleziona **Hardware accelerator: GPU**
3. Clicca **Save**

### Passo 3: Esegui il Notebook

1. Nel menu: **Runtime → Run all** (Esegui tutto)
2. Attendi ~3-5 minuti per il setup iniziale
3. Quando vedi l'interfaccia Gradio, sei pronto! 🎉

---

## 📱 Come Usare l'Interfaccia

### Modalità 1: Separazione Rapida (Consigliata per iniziare)

1. **Carica il file audio** (drag & drop o click)
2. **Scegli un preset** tra:
   - 🎤 Voce / Voce Femminile / Voce Maschile
   - 🎸 Strumentale
   - 🥁 Batteria
   - 🎹 Piano / Basso / Chitarra / Archi
   - 💬 Dialogo

3. **Seleziona la qualità:**
   - `fast` - Veloce (10-15 sec)
   - `balanced` - Bilanciato (20-30 sec) ⭐ Consigliato
   - `high` - Alta qualità (40-60 sec)

4. **Clicca "Separa Audio"**

5. **Risultati:**
   - 🎤 **Audio Estratto** = Il suono che hai scelto
   - 🎵 **Audio Residuo** = Tutto il resto
   - Clicca ⬇️ per scaricare i file

### Modalità 2: Separazione Personalizzata (Avanzata)

1. Carica il file audio
2. **Scrivi in inglese** cosa vuoi estrarre:
   - "A woman singing with high notes"
   - "Electric guitar solo with distortion"
   - "Applause and crowd cheering"
   - "Raindrops and thunder"

3. Seleziona qualità
4. Clicca "Separa Audio"

---

## 💡 Tips per Risultati Ottimali

### ✅ DO - Fai così:
- Usa file audio di **buona qualità** (WAV, FLAC meglio di MP3)
- Scrivi prompts **descrittivi e specifici**: "A woman singing opera" > "vocals"
- Prova **diversi prompts** se non sei soddisfatto
- Usa qualità **"high"** per produzioni finali
- **Salva subito** i risultati (potrebbero cancellarsi al refresh)

### ❌ DON'T - Evita:
- File audio troppo lunghi (max ~10 minuti)
- Prompts vaghi: "music" non funziona bene
- Aspettarti miracoli su audio di pessima qualità
- Chiudere il browser durante l'elaborazione

---

## 📊 Esempi di Utilizzo per Coreografi

### Caso 1: Creare Versione Strumentale
**Obiettivo:** Rimuovere voce da una canzone

1. Preset: **"Voce"**
2. Qualità: **"high"**
3. Risultato:
   - Audio Estratto = Solo voce (scarta)
   - **Audio Residuo = Strumentale** ✨ (usa questo!)

### Caso 2: Isolare Batteria per Sincronizzare Movimenti
**Obiettivo:** Solo ritmo/batteria

1. Preset: **"Batteria"**
2. Qualità: **"balanced"**
3. Risultato: Audio Estratto = Solo batteria

### Caso 3: Estrarre Solo Voce per Analisi Lirica
**Obiettivo:** Voce a cappella

1. Preset: **"Voce"** o **"Voce Femminile/Maschile"**
2. Qualità: **"high"**
3. Risultato: Audio Estratto = Solo voce pulita

### Caso 4: Pulire Registrazione Live
**Obiettivo:** Rimuovere pubblico/rumori

1. Modalità Personalizzata
2. Prompt: **"Music and performance without audience"**
3. Qualità: **"high"**
4. Risultato: Audio più pulito

---

## 🔧 Risoluzione Problemi

### ❌ Errore: "No GPU available"
**Soluzione:**
1. Runtime → Change runtime type → GPU
2. Restart runtime
3. Run all again

### ❌ Errore durante l'installazione
**Soluzione:**
1. Runtime → Restart runtime
2. Runtime → Run all
3. Se persiste, prova a ricaricare il notebook

### ❌ Risultati non soddisfacenti
**Prova:**
- Qualità "high" invece di "balanced"
- Riformula il prompt (più specifico)
- Verifica qualità audio originale
- Sperimenta con prompts diversi

### ❌ "Session crashed" o "Out of memory"
**Soluzione:**
- File audio troppo lungo → taglia in segmenti più corti
- Runtime → Restart runtime
- Prova modello "small" (modifica codice cella 5)

### ⏱️ Elaborazione lentissima
**Verifica:**
- Hai attivato la GPU? (vedi sopra)
- File non troppo lungo (max ~10 min)
- Colab non è sovraccarico (riprova più tardi)

---

## 📱 Accesso da Mobile

Il link Gradio (`https://xxxxx.gradio.live`) funziona su:
- 📱 Smartphone (iOS/Android)
- 📱 Tablet
- 💻 Qualsiasi browser

**Come:**
1. Copia il link dalla cella finale
2. Aprilo su smartphone/tablet
3. Interfaccia mobile-responsive automatica

⚠️ **Nota:** Il link è **temporaneo** (dura mentre la sessione Colab è attiva)

---

## 💾 Salvare il Notebook per Riutilizzo Futuro

### Opzione 1: Google Drive (Consigliata)
1. **File → Salva una copia in Drive**
2. Il notebook sarà sempre disponibile nel tuo Drive
3. Prossima volta: apri direttamente da Drive

### Opzione 2: Download Locale
1. **File → Download → Download .ipynb**
2. Salva sul computer
3. Ricarica su Colab quando serve

---

## 🎓 Workflow Completo per una Produzione

### Scenario: Creare Remix per Performance di Pattinaggio

1. **File originale:** `canzone_originale.mp3`

2. **Estrazione voce:**
   - Preset: "Voce"
   - Output: `voce_isolata.wav`

3. **Estrazione strumentale:**
   - Usa "Audio Residuo" del passo 2
   - Output: `strumentale.wav`

4. **Isola batteria (per sincro):**
   - Input: `strumentale.wav`
   - Preset: "Batteria"
   - Output: `batteria.wav`

5. **Editing finale:**
   - Usa `voce_isolata.wav` + `batteria.wav` + `strumentale.wav`
   - Remix in DAW (Audacity, Logic, Ableton)
   - Crea versione personalizzata

---

## ⏱️ Tempi di Elaborazione Stimati

| Durata Audio | Fast | Balanced | High |
|--------------|------|----------|------|
| 30 secondi   | ~5s  | ~10s     | ~20s |
| 1 minuto     | ~10s | ~20s     | ~40s |
| 3 minuti     | ~20s | ~45s     | ~90s |
| 5 minuti     | ~30s | ~75s     | ~150s|

*Tempi con GPU Tesla T4 (Colab standard)*

---

## 💰 Costi

### Colab Gratuito
- ✅ **Completamente gratuito**
- ⚠️ Limiti: ~2-3 ore consecutive
- ⚠️ GPU non sempre disponibile (priorità bassa)

### Colab Pro (€10/mese)
- ✅ Sessioni più lunghe (~24h)
- ✅ Priorità GPU (sempre disponibile)
- ✅ RAM aggiuntiva
- 💡 **Consigliato** se usi frequentemente

---

## 🔗 Link Utili

- **Repository SAM-Audio:** https://github.com/facebookresearch/sam-audio
- **Google Colab:** https://colab.research.google.com
- **Gradio Docs:** https://gradio.app/docs

---

## 📞 Supporto

### Problemi con il Notebook?
1. Controlla sezione "Risoluzione Problemi" sopra
2. Verifica che GPU sia attiva
3. Prova a riavviare runtime

### Domande su SAM-Audio?
- Tab "Info & Supporto" nel notebook
- Repository GitHub ufficiale
- Paper di ricerca

---

## 🎉 Sei Pronto!

Ora hai tutto per iniziare a usare SAM-Audio Studio per le tue produzioni.

**Prossimi passi:**
1. Apri il notebook su Colab
2. Attiva la GPU
3. Run all
4. Carica un file di test
5. Sperimenta!

**Buon lavoro!** 🎵✨
