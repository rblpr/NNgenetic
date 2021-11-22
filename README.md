# NNgenetic

# Structure

- Struttura delle classi:

  - Nel mondo si muovono agenti
    - Ogni agente ha un [id]
    - Un agente ha un cervello
      - Un cervello mantiene un id che permette un riferimento al suo agente ([idAgente]:[idCervello])
      - Un cervello ha un array di connessioni
        - Una connessione mantiene un riferimento al suo cervello ([idCervello]:[idConnessione])
        - Una connessione ha un neurone sorgente (sensoriale) e uno target (azione)
          - Un neurone mantiene un riferimento alla sua connessione ([idConnessione]:[idNeurone])

* Ogni componente deve comunicare solo con il suo wrapper:
  - neurone -> connessione -> cervello -> agente

# Esecuzione del NN

- Neurone sorgente:

  - risale all'agente su cui agisce
  - verifica la condizione
  - notifica il neurone target

- Neurone target:
  - risale all'agente su cui agisce
  - invoca l'azione necessaria sul suo agente

# TO DO

- [ ] Implementare gli id corrattemente
- [ ] Metodi per comunicare tra classi, nel modo descritto in [Structure]
