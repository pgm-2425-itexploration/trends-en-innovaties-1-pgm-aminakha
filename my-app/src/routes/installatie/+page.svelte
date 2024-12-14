<script>
    import Header from "../../components/partials/Header.svelte";
      import Footer from "../../components/partials/Footer.svelte";
      const scrollTo = (id) => {
          const element = document.getElementById(id);
          const offset = 100; // Adjust this value as needed
          const bodyRect = document.body.getBoundingClientRect().top;
          const elementRect = element.getBoundingClientRect().top;
          const elementPosition = elementRect - bodyRect;
          const offsetPosition = elementPosition - offset;
  
          window.scrollTo({
              top: offsetPosition,
              behavior: 'smooth'
          });
      }
    
  
  </script>

  <section class="installation-container">
    <Header />
    <div class="installation-content">
      <div class="installation-guide">
             <h1 id="frameworkinstallation">Framework installatie</h1>
      <p>De installatie van een framework kan soms een lastige klus zijn. Hieronder vind je een aantal stappen die je kunt volgen om een framework te installeren.</p>
      <h2>Downloaden van het framework</h2>
      <p>De eerste stap is het downloaden van het framework. Dit kan op verschillende manieren. Je kunt het framework downloaden van de website van de ontwikkelaar of je kunt het framework downloaden via een package manager zoals npm.</p>

      <code>
        <iframe width="100%" height="300" src="//jsfiddle.net/t6pjgz20/latest/embedded/js/dark/" frameborder="0" loading="lazy" allowtransparency="true" allowfullscreen="true"></iframe>      </code>
      <h2 id="sveltefiles">Svelte bestanden</h2>
      <p>Na het downloaden van het framework kun je beginnen met het maken van je eerste Svelte bestanden. Een Svelte bestand heeft de extensie .svelte en bevat HTML, CSS en JavaScript code.</p>
      <figure>
        <img src="/img/tut-1.png" alt="Tutorial 1" />
      </figure>
      <p>De folderstructuur wordt automatisch aangemaakt door het Svelte-framework, en je moet niet direct werken in de app.html. Je kunt echter wel de titel aanpassen en CSS- of JavaScript-bestanden koppelen.</p>
      <p>Je moet meer werken op de <strong>+page.svelte</strong> want daar gaat alles gerenderd worden voor de index.html (app.html)</p>
      <h3>Pagina's koppelen met .svelte-bestanden.</h3>
      <figure>
        <img src="/img/tut-2.png" alt="Tutorial 2" />
      </figure>
      
      <p>Om relative links aan te maken moet je een niewe map aanmaken met dezelfde benaming voor de link zoals op de  voorbeeld foto heb ik een folder about aangemaakt met erin een <strong>+page.svelte</strong></p>
      <h2 id="sveltecomponents">Svelte componenten</h2>
      <figure>
        <img src="/img/tut-3.png" alt="Tutorial 3" />
      </figure>
      <p>Naast Svelte-bestanden kun je ook Svelte-componenten maken. Een Svelte-component is een herbruikbaar stukje code dat je kunt gebruiken in meerdere Svelte-bestanden. Net zoals bij andere populaire frontend-frameworks werkt het importeren van componenten op dezelfde manier. Omdat je met Svelte alles in één bestand kunt doen, is het echter vaak handiger om je logica daar direct te beheren.</p>
      <h2 id="scopedcss">Scoped css</h2>
      
      <iframe width="100%" height="300" src="//jsfiddle.net/t6pjgz20/latest/embedded/html/dark/" frameborder="0" loading="lazy" allowtransparency="true" allowfullscreen="true"></iframe>    
      <p>Scoped css is een manier om stijlen toe te passen op een specifiek element in een Svelte-bestand. Dit is handig als je wilt dat de stijlen alleen van toepassing zijn op dat specifieke element en niet op andere elementen in het document.</p>
      <h2 id ="globalcss">Global css</h2>
      <iframe width="100%" height="300" src="//jsfiddle.net/t6pjgz20/latest/embedded/html/dark/" frameborder="0" loading="lazy" allowtransparency="true" allowfullscreen="true"></iframe>
      <p>Global css is een manier om stijlen toe te passen op alle elementen in een Svelte-bestand. Dit is handig als je wilt dat de stijlen van toepassing zijn op alle elementen in het document.</p>
      <h2 id="customcss">Custom properties</h2>
      <iframe width="100%" height="300" src="//jsfiddle.net/t6pjgz20/latest/embedded/html/dark/" frameborder="0" loading="lazy" allowtransparency="true" allowfullscreen="true"></iframe> 
           <p>Custom properties zijn variabelen die je kunt gebruiken om stijlen toe te passen op elementen in een Svelte-bestand. Dit is handig als je dezelfde stijlen op meerdere elementen wilt toepassen.</p>
      <h2>Nested css</h2>
      <iframe width="100%" height="300" src="//jsfiddle.net/t6pjgz20/latest/embedded/html/dark/" frameborder="0" loading="lazy" allowtransparency="true" allowfullscreen="true"></iframe>      <p>Nested css is een manier om stijlen toe te passen op geneste elementen in een Svelte-bestand. Dit is handig als je wilt dat de stijlen van toepassing zijn op alle geneste elementen in het document.</p>
      <h2 id="runtime">Run tijd</h2>
      <ol>
        <li>
           <h3>Minimale runtijd</h3> 
           <p>De runtime van Svelte is erg licht in vergelijking met frameworks zoals React of Vue . Na compilatie wordt alleen de essentiële code meegenomen, wat zorgt voor kleinere bundels en snellere laadtijden.</p>
          </li>
          <li>
            <h3>Reactiviteit</h3>
            <p>Svelte heeft een uniek reactiviteitsmodel zonder gebruik van een virtuele DOM. Tijdens runtime worden wijzigingen in de state direct toegepast op de DOM via gecompileerde code. Deze directe aanpak vermindert runtime-overhead en verbetert de prestaties.</p> 
          </li>
          <li>
            <h3>DOM-updates</h3>
            <p>De runtime voert efficiënte updates uit door specifieke DOM-elementen rechtstreeks te manipuleren, in plaats van een virtuele DOM te vergelijken.</p>
          </li>
          <li>
            <h3>Scoped styles</h3>
            <p>Stijlen die binnen een component worden gedefinieerd, blijven lokaal dankzij de runtime. Dit gebeurt door automatisch gegenereerde klassen of data-attributen, zodat stijlen niet conflicteren tussen componenten.</p>
          </li>
          <li>
            <h3>Animaties en transities</h3>
            <p>Svelte ondersteunt animaties en overgangen direct. De runtime bevat functies om deze effecten efficiënt toe te passen en te beheren.</p>
          </li>
          

      </ol>

      </div>

      <div class="tutorial-list">
        <h2>Begin</h2>
    <ul>
        <li><button  on:click={() => scrollTo('frameworkinstallation')}>Framework installation</button></li>
        <li><button  on:click={() => scrollTo('sveltefiles')}>Svelte bestanden</button></li>
        <li><button  on:click={() => scrollTo('sveltecomponents')}>Svelte componenten</button></li>
    </ul>
    
    <h2>Styles</h2>
    <ul>
        <li><button on:click={() => scrollTo('scopedcss')}>Scoped css</button><p></li>
        <li><button on:click={() => scrollTo('globalcss')}>Global css</button></li>
        <li><button on:click={() => scrollTo('customcss')}>Custom properties</button></li>
        <li><button on:click={() => scrollTo('nestedcss')}>Nested css</button></li>
    </ul>
    <h2>Run Tijd</h2>
    <ul>
        <li><button on:click={() => scrollTo('runtime')}>Run tijd</button></li>
    </ul>
    
    
    </div>
      
    </div>
    <Footer />

  </section>

  <style>
    .installation-container {
    
      & .installation-content { 
        &  .tutorial-list {
        width: 10rem;
        margin: 0 2rem;
        display: block;
            position: fixed;
            left: 60px;
            & button {
                background-color: #ffffff;
                border: solid 1px black;
                border-radius: 1rem;
                padding: 0.5rem 1rem;
                margin: 0.5rem 0;
                cursor: pointer;
                width: 100%;
                transition: all 0.3s ease;
                font-weight: 600;
                &:hover {
                    background-color: #ff7e5f;
                    transform: translateY(-0.2rem);
                    transition: all 0.3s ease;
                }
            }
        
        & h2 {
            font-size: 1.5rem;
            margin-top: 1rem;
        }
        & ul {
            list-style-type: none;
            padding: 0;
            & li {
                margin: 0.5rem 0;
                & a {
                    text-decoration: none;
                    color: black;
                    &:hover {
                        color: blue;
                    }
                }
            }
        }
    } 
         width: 100%;
      max-width: 80rem;
      justify-content: center;
      margin: 0 auto;
        display: flex;
        flex-direction: row-reverse;

        & .installation-guide  {
          width: 70%;
          padding: 1rem;
          & h1 {
            font-size: 2rem;
            margin-bottom: 1rem;
          }
          & h2 {
            font-size: 2rem;
            margin-top: 1rem;
            margin-bottom: 1rem;
          }
          & h3 {
            font-size: 1.2rem;
            margin-top: 1rem;
          }
          & p {
            font-size: 1.1rem;
            font-weight: 500;
            margin-top: 1rem;
            margin-bottom: 1rem;
          }
          & figure {
            margin-top: 1rem;
            & img {
              width: 100%;
              height: auto;
            }
          }
          & ol {
            margin-top: 1rem;
            margin-bottom: 1rem;
            & li {
              margin-top: 1rem;
            }
          }
          & code {
            margin-top: 1rem;
          }
        }
       
      }
    }
  </style>