# cpegedal.github.io
Projekter og instruktioner til CP Egedal.

# Vedligehold og nye artikler

Emner oprettes under `Instruktioner`.  Herunder oprettes et `_posts`-directory, og herunder oprettes artikler som bloc-posts.
Navnet på en artikel skal være `yyyy-mm-dd-min-fine-titel.markdown`.

Ved at bruge posting, kan Jekyll automatisk oprette indekssider og sortere artikerne.

Billeder skal lægges i `/assets/images/<artikelnavn>/`.  Du kan enten gemme dem her direkte, eller bruge scriptet i `/bin/update_images.py` til at finde alle billeder ved siden af artiklen og flytte dem det rigtige sted hen.  Hvis man tager et screenshot og paster ind i VSCode, gemmer VScode billedet samme sted som den artikel man redigerer.


Et helt eksempel:  En ny artikel under `Instruktioner/ESP32/_posts`

1. Opret en fil `2023-12-04-ESP32-som-webserver.markdown`
2. Start artiklen med disse linjer YAML i toppen:
```
    ---
    title: ESP32 som webserver
    layout: single
    tags: programmering
    ---
```
3. Skriv nu artiklen
4. Du tager et screenshot og ctrl-v in i artiklen.  Der kommer et link og en fil bliver
   oprettet ved siden af artiklen.
```
    ![Alt text](image.png)
```

## Linke mellem posts?

Hvis du vil lave et link mellem to posts, skal du bruge `/kate/gorier/<filnavn unden dato>/`.  Eksempel: `[her](/instruktioner/esp32/microPython-programstruktur)`

Når artiklen er færdig kan du køre `/bin/update_images.py Instruktioner/ESP32/_posts/2023-12-04-ESP32-som-webserver.markdown`.  Det lille program flytter nu alle billeder til den rigtige sti under `/assets/images/...`

# Gode udvidelser til VSCode

- Luna Paint
- Draw.io Integration