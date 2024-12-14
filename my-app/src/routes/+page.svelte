<script>
  import Header from "../components/partials/Header.svelte";
    import Chart from "../components/design/Chart.svelte";
    import Footer from "../components/partials/Footer.svelte";
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
<section class="home-container">
    <Header />
<main>
  <div id="hero" class="top-content">
    <div class="intro-svelte">
        <h2>Svelte</h2>
        <div class="blog">
            <div class="blog__intro">
                <p>Svelte is een front-endframework dat zorgt voor een snelle en efficiënte ontwikkeling van webapplicaties.</p>
                <p>Het biedt een snellere runtime en een verbeterde ervaring voor ontwikkelaars, zonder de overhead van andere frameworks.</p>
                <p>Met Svelte kunnen ontwikkelaars zich richten op het schrijven van code in plaats van zich zorgen te maken over complexe configuraties en optimalisaties.</p>
                <p class="blog__link"><a href="/installatie">Installeer Svelte 
                    <svg xmlns="http://www.w3.org/2000/svg"  viewBox="0 0 16 16" class="bi bi-arrow-right-short"><path fill-rule="evenodd" d="M4 8a.5.5 0 0 1 .5-.5h5.793L8.146 5.354a.5.5 0 1 1 .708-.708l3 3a.5.5 0 0 1 0 .708l-3 3a.5.5 0 0 1-.708-.708L10.293 8.5H4.5A.5.5 0 0 1 4 8z"/></svg></a></p>   
            </div>
       
        </div>
 
</div>
    
    <figure>
    <img src="/img/svelte.svg" alt="Logo Svelte">
</figure>
  </div>
 <div class="trend-container">
    <div class="trend__content">
        <div class="trend__title">

        <h2><img src="/img/chart-simple-svgrepo-com.svg" alt="Chart">Populariteit Svelte framework</h2>
    </div>

    <div class="trend__chart-and-description">
        <Chart />

        <div class="trend__chart-and-description-container">
<div class="trend__description">
    <h3>Wat is svelte ?</h3>
        <p>Svelte is een opkomend framework dat steeds populairder wordt en naar verwachting in 2024 een grotere impact zal hebben.</p>

    <p>Het onderscheidt zich van andere frameworks door zijn unieke benadering van het bouwen van webapplicaties, waarbij het compileert naar efficiënte, pure JavaScript-code in plaats van gebruik te maken van virtuele DOM's. Hierdoor biedt Svelte voordelen op het gebied van prestaties en eenvoud.</p>
    
    <p>Het wordt steeds vaker gekozen door ontwikkelaars vanwege de gebruiksvriendelijke syntaxis, de snelle leercurve en de uitstekende prestaties.</p>
    
    <p>Naarmate meer bedrijven en ontwikkelaars Svelte omarmen, zal de populariteit ervan naar verwachting blijven groeien in 2024 en de jaren daarna.</p>
    </div>

    <div class="trend__description">
        <h3>Toekomstige ondersteuning verwacht ? </h3>
        <p>Svelte wordt steeds meer ondersteund en geprezen als een toekomstgerichte technologie voor webontwikkeling.</p>  
<p>Dankzij de focus op efficiëntie, gebruiksvriendelijke tooling en een sterke community groeit de adoptie gestaag.</p>  
<p>Grote bedrijven en ontwikkelaars omarmen Svelte vanwege de snelle laadtijden, minimale bundelgrootte en eenvoud in gebruik.</p>  
<p>Met voortdurende updates, ondersteuning door tools zoals SvelteKit, en integratie in moderne workflows lijkt Svelte klaar om een belangrijke rol te spelen in de toekomst van frontend-ontwikkeling.</p>
    </div>

        </div>
    
    
    </div>
    </div>
    
    
 </div>

   <div  class="websites-container">
    <div class="websites-container--content">
        <div class="websites-title--center">
                     <h2 id="websites" class="websites-title" ><img src="/img/company-svgrepo-com.svg" alt="Company">Bekende bedrijven die Svelte gebruiken </h2>

        </div>
        
    <div class="websites-container--flex"> 
        <ul >
        <li>
            <button on:click={() => scrollTo('apple')} ><img src="/img/apple.png" alt="Apple"> Apple</button>
            
        
        </li>
        <li>
            <button on:click={() => scrollTo('spotify')} ><img src="/img/spotify.png" alt="Spotify">Spotify</button>
           
        </li>
        <li>
            <button on:click={() => scrollTo('sky')} ><img src="/img/sky.png" alt="Sky news">Sky news</button>

            
        </li>
        <li>
            <button on:click={() => scrollTo('ny')} ><img src="/img/ny-times.png" alt="New york times">New York Times</button>

           
            
        </li>
        <li>
            <button on:click={() => scrollTo('stackoverflow')} ><img src="/img/stackoverflow.svg" alt="Stackoverflow">Stackoverflow</button>

            
        </li>
        <li>
            <button on:click={() => scrollTo('yelp')} ><img src="/img/yelp.png" alt="Yelp ">Yelp</button>

        </li>
       
    </ul>    
    </div>
    <ul class="website-description-container">
        <li>
        <h2 id="apple">Apple</h2>
        <div class="company-description">
             <img src="/img/apple.png" alt="Apple">
             <div class="company-description--flex">
                <p>Apple heeft Svelte geïmplementeerd in verschillende projecten, waaronder de Apple Music-website en de Apple Store.</p> 
        <p>De keuze voor Svelte is gebaseerd op de prestaties en de eenvoud van het framework, waardoor Apple snellere en efficiëntere webapplicaties kan bouwen.</p>
        </div>
             </div>
        
       
        

        </li>
        <li>
        <h2 id="spotify">Spotify</h2>
        <div class="company-description">
             <img src="/img/spotify.png" alt="Spotify">
             <div class="company-description--flex">
                <p>Spotify maakt gebruik van Svelte in de ontwikkeling van de webversie van zijn muziekstreamingdienst.</p>
        <p>De keuze voor Svelte is gebaseerd op de snelheid en de eenvoud van het framework, waardoor Spotify een snelle en responsieve webervaring kan bieden aan zijn gebruikers.</p>
        </div>
             </div>

        </li>
        <li>
        <h2 id="sky">Sky news</h2>
        <div class="company-description">
             <img src="/img/sky.png" alt="Sky news">
             <div class="company-description--flex">
                <p>Sky News heeft Svelte geïmplementeerd in de ontwikkeling van zijn nieuwswebsite.</p>
        <p>De keuze voor Svelte is gebaseerd op de prestaties en de eenvoud van het framework, waardoor Sky News snel en efficiënt webcontent kan leveren aan zijn gebruikers.</p>
        </div>
             </div>
        </li>
        <li>
        <h2 id="ny">New York Times</h2>
        <div class="company-description">
             <img src="/img/ny-times.png" alt="New York Times">
             <div class="company-description--flex">
                <p>The New York Times heeft Svelte geïmplementeerd in de ontwikkeling van zijn website en webapplicaties.</p>
        <p>De keuze voor Svelte is gebaseerd op de prestaties en de eenvoud van het framework, waardoor The New York Times snel en efficiënt webcontent kan leveren aan zijn lezers.</p>
        </div>
             </div>
        </li>
        <li>
        <h2 id="stackoverflow">Stackoverflow</h2>
        <div class="company-description">
                <img src="/img/stackoverflow.svg" alt="Stackoverflow">
                <div class="company-description--flex">
                    <p>Stack Overflow maakt gebruik van Svelte in de ontwikkeling van zijn webapplicaties en tools.</p>
                    <p>De keuze voor Svelte is gebaseerd op de prestaties en de eenvoud van het framework, waardoor Stack Overflow snelle en efficiënte webervaringen kan bieden aan zijn gebruikers.</p>
                </div>

        </div>
        <li>
        <h2 id="yelp">Yelp</h2>
        <div class="company-description">
                <img src="/img/yelp.png" alt="Yelp">
                <div class="company-description--flex">
                    <p>Yelp heeft Svelte geïmplementeerd in de ontwikkeling van zijn website en webapplicaties.</p>
                    <p>De keuze voor Svelte is gebaseerd op de prestaties en de eenvoud van het framework, waardoor Yelp snel en efficiënt webcontent kan leveren aan zijn gebruikers.</p>
                </div>
            
        </li>
       
            <button on:click={() => scrollTo('hero')} ><img src="/img/arrow-right.svg" alt="Arrow "></button>

    </ul>
    

    </div>
   
   

    
   </div>
</main>
<Footer />
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
        
        width: 100%;
        background: linear-gradient(180deg, #ff7e5f, #f75d59);
        background-size: 400% 400%;
        animation: gradientAnimation 10s ease infinite;
        color: white;
        margin: 0 auto;
      gap:2rem;
        & .blog__link {
            width: 100%;
            text-align: center;
            display: flex;
                   & a {
                    padding:.5rem 1rem;
                    display: flex;
                    align-items: center;
                    color:white;
                    text-decoration: none;
                    background-color: white;
                    border-radius: 1rem;
                    color:black;
                    transition: all 0.3s;
                    &:hover {
                        background: #ffa474;
                color: #000;
                box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
                transform: translateY(-3px);
                        transition: all 0.3s;
                    }
                   }
                    & svg {
                        width: 3rem;
                        
                        margin-left: 0.5rem;
                    }
                }
         & p {
            font-size: 1.2rem;
            margin-right: 2rem;
            width: 51rem;
            margin-top: 1rem;
         }
        & h2 {
            font-size: 3rem;
            margin-right: 2rem;
        }
        & figure {
            width: 15rem;
            height: 15rem;
            
            & img {
                width: 100%;
                height: 100%;
                object-fit: contain;
                box-shadow: 1px 1px 5px rgba(255, 255, 255, 0.5);
                border-radius: 1rem;
                padding: 1rem;
            }
        }
        
    }
    
    .trend-container {

        margin-top: 2rem;
        margin-bottom: 2rem;
                & .trend__content {
            width: 100%;
        max-width: 80rem;
        margin: 0 auto;

        & .trend__chart-and-description {
            display: flex;
            gap:1rem;
            align-items: flex-start;
            margin-top: 2rem;
            
            & .trend__chart-and-description-container {
                display: flex;
                flex-direction: column;
                gap: 1rem;
            }
        }

        & .trend__title {
            display: flex;
            justify-content: center;

             & h2 {
                & img {
                    width: 2rem;
                    height: 2rem;
                    margin-right: 1rem;
                }
            font-size: 2rem;
            margin-bottom: 1rem;
            
            background-color: black;
            border-radius: 1rem ;
            color: white;
            padding: 1rem 2rem;
            display: inline-flex;
        
            
      text-align: center;
         }
        }
       
         & .trend__description {
            padding:1.5rem;
            border: solid 2px #b0b0b0;
          & h3 {
            margin-left: 2rem;
                margin-bottom: 1rem;
                font-size: 1.4rem;

          }
           
            
            width: 42rem;
            border-radius: 1rem;
            background-color: white ;
         }
        & p{
  
          padding-left:2rem;
            padding-bottom: 1rem;
        font-family: Arial, sans-serif;
        font-size: 1.2rem;
        width: 38rem;
        font-size: medium;
        font-size: 15px;
        
        
          
        }
        }
        
    }
.websites-container {
    background-color: #775f93;

    & .websites-container--content {
            width: 100%;
    max-width: 80rem;
    margin: 0 auto;
    & .websites-title--center {
        display: flex;
         & .websites-title {
        display: inline-flex;
        padding: 1rem 2rem;
        border-radius: 1rem;
            justify-content: center;
            align-items: center;
            margin:0 auto;
background-color: black;
color: white;
            margin-top: 2rem;
                & img {
                    width: 2rem;
                    height: 2rem;
                    margin-right: 1rem;
                }
            font-size: 2rem;
            margin-bottom: 1rem;
            
            
            border-radius: 1rem ;
            color: white;
            padding: 1rem 2rem;
            display: inline-flex;
        
            
      text-align: center;
         
    }
    }
   
    }
    & .websites-container--flex {
    display: flex;
    flex-direction: column;
    justify-items: center;
    margin-top:2rem;
    align-items: center;
    }
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
            border-radius: 1rem;
            transition: all ease-in-out 0.3s;
            &:hover {
                box-shadow: 0 4px 8px rgba(245, 61, 0, 0.5);
            }
           & button {
        
                    width: 100%;
            border: solid 1px #333;
            height: 13rem;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-between;
            border-radius: 1rem;
            background:none;
            cursor: pointer;
                
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

    & .website-description-container {
        display: flex;
        flex-direction: column;
        gap:1rem;
        & button {
            width: 8rem;
        display: flex;
            justify-content: center;
            align-items: center;
            background-color: white;
            cursor: pointer;
            border-radius: 1rem;
            
            transition: all 0.3s ease-in-out;
           &:hover {
            box-shadow: -6px 6px black;
            transform: translateY(-3px) translateX(3px);
            transition: all 0.3s ease-in-out;
           }
            & img {
                width: 3rem;
           
                
                
                transform: rotate(270deg);
            }
        }
        & li {
            padding:1rem;
            width: auto;
            border: solid 2px #b0b0b0;
             display: flex;
        flex-direction: column;
        & h2 {
                margin:0;
                padding:0;
            }
        & .company-description {
            & .company-description--flex {
                display: flex;
                flex-direction: column;
                gap: 1rem;
            }
            & img {
                box-shadow: 1px 1px 5px rgba(255, 255, 255, 0.5);
                border-radius: 1rem;
            }
            display: flex;
            align-items: center;
            & p {
                width: auto;
            }
            
        }
        }
       
    }
}

@keyframes gradientAnimation {
        0% {
            background-position: 0% 50%;
        }
        50% {
            background-position: 100% 50%;
        }
        100% {
            background-position: 0% 50%;
        }
    }
  
</style>
