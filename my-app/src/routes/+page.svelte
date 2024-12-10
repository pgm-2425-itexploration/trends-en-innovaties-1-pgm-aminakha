<script>
  import Header from "../components/partials/Header.svelte";
</script>
<section class="home-container">
    <Header />
<main>
  <div class="top-content">
    <div class="info-svelte">
        <h2>Wat is Svelte ?</h2>
    <div class="description-svelte">
      <p>
        <strong>Svelte</strong> is een modern JavaScript-framework waarmee je snelle
        en interactieve webapplicaties kunt bouwen. In tegenstelling tot traditionele
        frameworks zoals React of Vue werkt Svelte op een unieke manier:
      </p>
      <ol>
        <li>
          <h3>Geen Virtual DOM</h3>
          <p>Svelte gebruikt geen virtual DOM. In plaats daarvan compileert het je code naar zeer efficiënte JavaScript die direct de DOM bijwerkt.</p>
        </li>
        <li>
            <h3>Reactieve Ontwikkeling</h3>
            <p>Met Svelte is reactiviteit eenvoudig. Je hoeft alleen waarden aan variabelen toe te wijzen, en de UI wordt automatisch bijgewerkt – geen ingewikkelde state management tools nodig.</p>
        </li>
        <li>
            <h3>Lichtgewicht</h3>
            <p>Omdat Svelte je app tijdens het bouwproces compileert, is het eindresultaat klein en geoptimaliseerd.</p>
        </li>
        <li>
            <h3>Eenvoudige Syntax</h3>
            Svelte-bestanden combineren HTML, JavaScript en CSS in één bestand (.svelte), wat het gemakkelijk maakt om te leren en gebruiken.
        </li>
      </ol>
      
  
    </div>

    
    </div>
    <figure>
    <img src="/logo-svelte.png" alt="Logo Svelte">
</figure>
  </div>
 
   <div  class="websites-container">
    <h2 id="websites" >Websites die Svelte gebruiken</h2>
    <ul>
        <li>
            <img src="/img/apple.png" alt="Apple">
            <p>Apple</p>
        </li>
        <li>
            <img src="/img/spotify.png" alt="Spotify">
            <p>Spotify</p>
        </li>
        <li>
            <img src="/img/sky.png" alt="Sky">
            <p>Sky news</p>
        </li>
        <li>
            <img src="/img/ny-times.png" alt="New York times">
            <p>New York Times</p>
        </li>
        <li>
            <img src="/img/food.svg" alt="Food">
            <p>Food</p>

        </li>
        <li>
            <img src="/img/yelp.png" alt="Yelp">
            <p>Yelp</p>
        </li>
       
    </ul>
   </div>
</main>
</section>


<style>
   
    .home-container {
        scroll-behavior: smooth;
    }
    .top-content {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 2rem;
        border: solid 2px #333;
        border-radius: 1rem;
        width: 100%;
        max-width: 80rem;
        margin: 0 auto;
        margin-top: 1rem;
        & .info-svelte {
            & h2 {
                font-size: 2rem;
                margin-bottom: 1rem;
            }
            & .description-svelte {
                & p {
                    width: 40rem;
                    margin-bottom: 1rem;
                    font-size: 1rem;
                }
            }
            
        }
        
    }
    
.websites-container {
    display: flex;
    flex-direction: column;
    justify-items: center;
    margin-top:2rem;
    align-items: center;
    & h2 {
        font-size: 2rem;
        margin-bottom: 1rem;
        
    }
    & ul  {
        display: grid;
        grid-template-columns: repeat(3, 13rem);
    padding: 1rem; /* Adds padding around the container */
    justify-items: center; /* Centers the content inside each grid item */
    align-items: center; /* Centers the content vertically */
    gap:1rem;
        & li {
width: 100%;
            border: solid 1px #333;
            height: 13rem;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-between;
            border-radius: 1rem;
            transition: all ease-in-out 0.3s;
            &:hover {
                box-shadow: 0 4px 8px rgba(245, 61, 0, 0.5);
            }
            & p {
                font-size: 1.2rem;
                font-weight: bold;
                margin-bottom:1rem
            }
            & img {
                &:first-of-type {
                    width: 8rem;
                    height: 8rem;
                }
                width: 10rem;
                height: 10rem;
                margin: 1rem;
                object-fit: contain;
            }
        }
    }
}
    
  
</style>
