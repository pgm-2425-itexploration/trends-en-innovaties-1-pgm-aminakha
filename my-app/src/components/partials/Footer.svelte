<script>
    // You can add any JavaScript logic here if needed
</script>

<style>
    footer {
        text-align: center  ;
        & .footer-content {
            & .author-description {
                & .social-container {
                    display: flex;
                    & img {
                        width: 2rem;
                        margin: 0.5rem;
                        border-radius: 1rem;
                    }
                }
            }
            gap: 1rem;  
          
             width: 100%;
        max-width: 80rem;
        display: flex;
       justify-content: center;
        margin:0 auto;
        margin-bottom: 1rem;
        & .links-container {
            display: flex;
            flex-direction: column;
            padding-bottom:2rem;
            & li {
                & a {
                    color:white;
                }
            }
           
        }
        & h3 {
            font-size: 1.5rem;
            
        
        }
        }
        background-color: #333;
        color: white;
        padding: 1rem;
      
    }
</style>

<footer>
    <div class="footer-content">
        <div class="author-description">
              <h3>Amin Akhayad </h3>
              <div class="social-container">
                <a href="https://www.linkedin.com/in/amin-akhayad-1b60a62b5"><img src="/img/linkedin-rounded-svgrepo-com.svg" alt="linkedin"></a>
                <a href="https://github.com/AminAkhayad"><img src="/img/github-142-svgrepo-com.svg" alt="github"></a>
              </div>
        </div>
      
       <div class="links-container">
        <h3>Links</h3>
         <ul>
            <li><a href="/">Home</a></li>
            <li><a href="/installatie">Installatie</a></li>
    </ul>
       </div>
       
    </div>
    
    <p>&copy; {new Date().getFullYear()} Amin All rights reserved.</p>
</footer>