<script>
  import Header from "../components/partials/Header.svelte";
</script>
<section class="home-container">
    <Header />
<main>
  <div class="top-content">
    <div class="intro-svelte">
        <h2>Svelte</h2>
        <div class="blog">
            <div class="blog__intro">
                <p>Svelte is een front-endframework dat zorgt voor een snelle en efficiënte ontwikkeling van webapplicaties.</p>
                <p>Het biedt een snellere runtime en een verbeterde ervaring voor ontwikkelaars, zonder de overhead van andere frameworks.</p>
                <p>Bekijk waarom je dit zou gebruiken.</p>
                <p class="blog__link"><a href="#">Waarom Svelte een topkeuze is voor frontend 
                    <svg xmlns="http://www.w3.org/2000/svg"  viewBox="0 0 16 16" class="bi bi-arrow-right-short"><path fill-rule="evenodd" d="M4 8a.5.5 0 0 1 .5-.5h5.793L8.146 5.354a.5.5 0 1 1 .708-.708l3 3a.5.5 0 0 1 0 .708l-3 3a.5.5 0 0 1-.708-.708L10.293 8.5H4.5A.5.5 0 0 1 4 8z"/></svg></a></p>   
            </div>
       
        </div>
 
</div>
    
    <figure>
    <img src="/img/svelte.svg" alt="Logo Svelte">
</figure>
  </div>
 
   <div  class="websites-container">
    <div class="websites-container--content">
         <h2 id="websites" >Bekende bedrijven die Svelte gebruiken </h2>
    <div class="websites-container--flex">
     <ul >
        <li>
            <p><a href="#apple"><img src="/img/apple.png" alt="Apple"> Apple</a></p>
            
        
        </li>
        <li>
            <p><a href="#spotify"><img src="/img/spotify.png" alt="Spotify">Spotify</a></p>
        </li>
        <li>
            <p><a href="#sky"><img src="/img/sky.png" alt="Sky">Sky news</a></p>
            
        </li>
        <li>
            <p><a href="#ny"><img src="/img/ny-times.png" alt="New York times">New York Times</a></p>
            
        </li>
        <li>
            <p><a href="#food"><img src="/img/stackoverflow.svg" alt="Food">Food</a></p>
        </li>
        <li>
            <p><a href="#yelp"><img src="/img/yelp.png" alt="Yelp">Yelp</a></p> 
        </li>
       
    </ul>    
    </div><h2 id="apple">Apple</h2>
    </div>
   
   

    
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
    
.websites-container {
    background-color: #775f93;

    & .websites-container--content {
            width: 100%;
    max-width: 80rem;
    margin: 0 auto;
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
            & p {
                font-size: 1.2rem;
                font-weight: bold;
                border-radius: 1rem;
                width: 100%;
                & a {
                    width: 100%;
            border: solid 1px #333;
            height: 13rem;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-between;
            border-radius: 1rem;
                }
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
