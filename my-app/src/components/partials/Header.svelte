<script>
    // Reactive variable to store the theme state
    let isDarkMode = false;

    // Function to toggle the theme
    function toggleDarkMode() {
        isDarkMode = !isDarkMode;
        if (isDarkMode) {
            document.documentElement.classList.add('dark');
        } else {
            document.documentElement.classList.remove('dark');
        }
    }
</script>

<header class={isDarkMode ? 'dark' : 'light'}>
    <h1>Svelte Tutorial</h1>
    <nav>
        <ul>
            <li><a href="/">Home</a></li>
            <li><a href="/about">About</a></li>
            <li><a href="/contact">Contact</a></li>
        </ul>
        <div class="darkswitch-container">
            <button on:click={toggleDarkMode} class="darkswitch">
                {isDarkMode ? '☀️ Light Mode' : '🌙 Dark Mode'}
            </button>
        </div>
    </nav>
</header>

<style>
/* Light theme styles */
header {
    padding: 10px 0;
    font-family: 'Roboto', sans-serif;
    display: flex;
    justify-content: space-between;
    padding: 1rem;
    & h1 {
        font-family: monospace;
    }
   &.light{
    background-color: #f5f5f5;
    color: #333;
    & nav {
        display: flex;
        & ul {
            font-family: monospace;
                display: flex;
                justify-content: space-between;
                padding-right: 1rem;
                border-right: solid 1px #333;
                align-items: center;
                gap: 1rem;
                text-transform: uppercase;
                font-size: 1.2rem;
                        & li {
                & a {
                    color: #333;
                    font-family: monospace;
                    &:hover {
                        background-color: #e0e0e0;
                        
                    }
                }
            }
        }
    }

   
    & .darkswitch  {
        margin-left:1rem;
          background-color: black;
    color: white;
    }
} 
&.dark {
    background-color: #333;
    color: #fff;
    & nav {
        
            display: flex;
        & ul {
            font-family: monospace;
                display: flex;
                justify-content: space-between;
                padding-right: 1rem;
                border-right: solid 1px white;
                align-items: center;
                gap: 1rem;
                text-transform: uppercase;
                font-size: 1.2rem;
                        & li {
                & a {
                    color: #333;
                    font-family: monospace;
                    &:hover {
                        background-color: #e0e0e0;
                        
                    }
                }
            }
            & li {
                & a {
                     color: #fff;
                }
            }
        }
    }
    & .darkswitch {
        margin-left:1rem;
    background-color: white;
    color: black;    
    }
}
}



/* Shared styles */



.darkswitch-container {
    margin-left: auto;
}

.darkswitch {
    border: 1px solid black;
    border-radius: 5px;
    padding: 0.5rem 1rem;
    cursor: pointer;
    transition: background-color 0.3s, color 0.3s;
}


</style>
