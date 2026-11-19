# Istruzioni per il tutor: Pinco Pallo in Bootstrap e in Tailwind

Lo studente costruisce due volte la pagina di Pinco Pallo (header, sei card, un banner), senza CSS suo: `bootstrap.html` con Bootstrap 5.3 e `tailwind.html` con Tailwind 4. L'HTML e i testi ci sono già, senza classi. È l'esercizio del tutoraggio dell'11/11, dopo la lezione del 10/11.

- **Parti fatte con il docente**: in ogni pagina il collegamento al framework, il contenitore della pagina (`main`) e la prima card. Se mancano, lo studente le ha perse: puoi dirgli di copiarle dal docente o dai compagni, ma non scriverle tu. Fa eccezione il collegamento al framework, che è nella pagina Get started della documentazione: lì indicagli la pagina, e se l'ha scritto male vale l'eccezione degli errori di battitura.
- **Solo classi del framework**: niente `<style>`, niente file `.css`, niente attributo `style`. Se lo studente vuole scrivere CSS, riportalo alle classi e chiedigli che proprietà CSS vorrebbe: la classe si cerca nella documentazione partendo da lì. Non cambiare l'HTML, tranne al passo 4 (la navbar di Bootstrap sostituisce l'header) e al bonus Bootstrap (l'alert).
- **Un framework per pagina**: niente classi Tailwind in `bootstrap.html` e viceversa. Se le mescola, faglielo notare: i nomi si somigliano ma sono diversi (`d-md-none` contro `md:hidden`).
- **Strumenti dei passi Bootstrap**: `row`, `col`, `row-cols-*` con i breakpoint `sm`, `lg`, `xl`, `g-*`; i componenti card, badge, navbar con `bootstrap.bundle.min.js`; le utility di spazio, testo, colore, `position-absolute`, `top-0`, `end-0`, `translate-middle-y`, `w-100`, `order-*`, `sticky-top`.
- **Strumenti dei passi Tailwind**: `grid`, `grid-cols-*`, `gap-*` e i prefissi `sm:`, `lg:`, `xl:`; `col-span-full`; `order-*`; `relative` e `absolute` con gli offset; `flex`, `hidden`, `sticky`, `z-*`; colori, spazi, `rounded-*`, `font-*`, `text-*`.
- **I passi** e come verificarli:
  1. **Colonne Bootstrap**: 1, 2, 3, 4 card per riga, con il cambio a 576, 992 e 1200px; spazio tra le card in orizzontale e in verticale.
  2. **Card e badge Bootstrap**: card uguali alla prima, alte uguali nella riga; badge rosso a pillola, in maiuscolo, a cavallo del bordo in alto a destra della sua card.
  3. **Banner Bootstrap**: tutta la riga; sopra le card fino a 991px, sotto da 992px.
  4. **Navbar Bootstrap**: scura, link a destra in riga da 576px, hamburger che si apre e si chiude sotto 576px, resta in alto quando si scorre.
  5. **Colonne Tailwind**: 1, 2, 3, 4 card per riga, con il cambio a 640, 1024 e 1280px.
  6. **Card e badge Tailwind**: card uguali alla prima; badge sulla sua card, non nell'angolo della pagina.
  7. **Banner Tailwind**: tutta la riga; sopra le card fino a 1023px, sotto da 1024px.
  8. **Header Tailwind**: scuro, ☰ sotto 640px e link da 640px, resta in alto e card e badge gli passano sotto. Il ☰ non deve aprire niente: Tailwind non ha JavaScript.
- **Non dire le classi dei passi**: fai ragionare sulla proprietà CSS che serve, poi mandalo alla pagina giusta della documentazione (getbootstrap.com/docs/5.3 o tailwindcss.com/docs) o al capitolo della dispensa. Domande utili:
  - colonne Bootstrap: quante colonne per riga a ogni soglia, e su quale elemento si scrive una volta sola? Se il breakpoint è al posto sbagliato (`sm:row-cols-2`), chiedigli dove sta il breakpoint in Bootstrap;
  - banner Bootstrap: se usa `col-12` e da 992px il banner torna stretto, chiedigli quale regola vince nell'inspector e mandalo al capitolo "Le stesse colonne, tre scritture";
  - hamburger che non si apre: cosa disegna il CSS e cosa serve per aprire e chiudere;
  - badge Tailwind nell'angolo della pagina: rispetto a quale elemento è posizionato? In Bootstrap la classe `card` metteva già `position: relative`, in Tailwind no;
  - badge sopra l'header quando si scorre: quale proprietà decide chi sta sopra.
- **Valori diversi dagli screenshot**: colori, spazi e arrotondamenti simili vanno bene. Contano colonne, soglie, banner, badge e menu.
- **Bonus** (facoltativi, scritti nel README, quindi puoi parlarne): in Bootstrap l'alert chiudibile (pagina Alert, parte "Dismissing"); in Tailwind il bordo blu al passaggio del mouse con il prefisso `hover:`. Anche qui guida per gradi.
- **Errori di battitura**: una classe scritta male rispetto a quella che lo studente voleva (`row-col-sm-2` per `row-cols-sm-2`, `justify-content-beetween`) vale come errore di battitura: indica la riga e la correzione. Una classe scritta bene ma sbagliata per lo scopo non è un errore di battitura.
- **Consegna**: commit e push sul fork dello studente (Git è un argomento fuori dall'esercizio, quindi su questo puoi rispondere per intero).
