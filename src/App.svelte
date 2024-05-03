<!-- App.svelte -->
<script>
    let currentPage = 'home'; // Initialize currentPage to home

    // Function to handle button clicks and update currentPage
    function handleClick(page) {
        currentPage = page;
    }
</script>
{#if currentPage === 'home'}
<div class="container">
    <h1>Hannah's Honors Thesis</h1>
    <div class="paragraph-container">
        <p>Behold the wonders of an honors thesis creative portfolio by Senior Hannah Allison, a whimsical fusion of 2D animation and computer science sorcery. Hannah, a double major in mathematics and CS in just one semester combined the alchemy of JavaScript, HTML, and CSS, vibrant drawings come to life in an interactive display crafted for a bookstore. Embark on a journey where imagination intertwines with technology, inviting you to explore a realm where every line and pixel tells a tale! </p>
    </div>
    <p></p>
    <div class="button-container">
        <button id="contributors-button" on:click={() => handleClick('contributors')}>Sorcerers of Support</button>
        <div>
            <button id="cs-button" on:click={() => handleClick('cs')}>CS</button>
            <button id="art-button" on:click={() => handleClick('art')}>ART</button>
        </div>
    </div>
</div>
{:else if currentPage === 'contributors'}
<div class="container">
    <h3>A huge thank you to everyone who helped bring this project to life:</h3>
    <div class="contrubutors" >
    <div class="paragraph-container">
        <h3>With the wisdom of wizards, the Thesis Committee:</h3>
        <p><strong>Tim Richards</strong><br>
            Senior Teaching Faculty, CICS<br>
            Committee Chair</p>
        <p><strong>Hallie Bahn</strong><br>
            Assistant Professor, Art<br>
            Committee Member</p>

        <h3>To everyone at UMass Libraries, including:</h3>
        <p><strong>Kim Fill</strong><br>
            Events, Exhibits, and Outreach Coordinator</p>
        <p><strong>Steve Acquah</strong><br>
            Coordinator, Digital Media Lab</p>
        <h3>Friends and family for their unwavering support:</h3>
        <p>(Special thanks to Mom, Dad, Eva, Hadas, Eryn, Sana, and all who contributed their magic, big or small)</p>
      </div>
    </div>
    <button id="back-to-home-button" on:click={() => handleClick('home')}>Back</button>
    </div>
{:else if currentPage === 'cs'}
<div class="container">
    <h1>CodeCrafters Hub</h1>
    <div class="paragraph-container">
    <p1>Step into a digital realm where the elements of JavaScript, HTML, and CSS converge to weave captivating animations that dance across your screen. Within these animations lies embedded magic – JavaScript spells that imbue them with life and interactivity, responding to your every touch. These enchanting animations have been transformed into JavaScript and HTML, seamlessly merging with Svelte projects to create a spellbinding web experience. Guided by a mystical Node.js backend, the project taps into the whispers of a hidden library, unveiling a trove of knowledge with each interaction.</p1>
    </div>
    <button id="back-to-home-button" on:click={() => handleClick('home')}>Back</button>
</div>
{:else if currentPage === 'art'}
<div class="container">
    <h1>Artistry Alcove</h1>
    <div class="paragraph-container">
    <p2>Enter Hannah's enchanting realm, where her handcrafted animations and props, inspired by classic fairy tales, come to life. By day, bask in the charm of her creations, and by night, behold their mystical transformation under the moon's gentle glow. Crafted with care and skill, Hannah first brought her visions to life using Adobe Animate before weaving them into the fabric of this magical experience. Every ten minutes, the magic unfolds, and a fairy flys!</p2>
    </div>
    <button id="back-to-home-button" on:click={() => handleClick('home')}>Back</button>
</div>
{/if}

<style>
    /* Add your CSS styles here */
    .container {
        position: absolute;
        top: 65px; /* Adjust the top position as per your requirement */
        left: calc((1536px - 500px) / 2 + 250px); /* Adjust the left position as per your requirement */
        width: 270px; /* Increase width */
        height: 550px; /* Increase height */
        background-color: #FAEBD7; /* Set light brown background color */
        border: 16px solid #63310e; /* Set dark brown border */
        padding: 20px;
        border-radius: 5px;
        /* overflow-y: auto; Enable scrolling if content overflows */
        z-index: 1; /* Ensure the container is above other elements */
        pointer-events: auto; /* Enable pointer events for the container */
        text-align: center; /* Center text horizontally */
        color: #8B4513; /* Set text color to dark brown */
        font-family: Chalkboard, sans-serif; /* Set font to Chalkduster */
    }
    .contrubutors {
        font-size: 12px;
    }
    h1 {
        margin-top: 10px; /* Lower the margin top */
        font-size: 20px;
    }
    h3 {
        margin-top: 5px; /* Lower the margin top */
        font-size: 15px;
    }
 
 

    .paragraph-container {
        background-color: #e3fad7; /* Set light brown background color */
        padding: 5px; /* Add padding */
        border-radius: 15px; /* Add border radius */
        margin-bottom: 10px; /* Add margin bottom */
        margin-top: 5px;
        width: 240px; /* Set width to auto */
        align-items: center;
        border: 4px solid #8B4513; /* Set dark brown border */
    }

    .button-container {
        margin-bottom: 10px; /* Add margin bottom */
    }

    button {
        font-size: 20px; /* Adjusted font size */
        padding: 8px 15px; /* Adjusted padding */
        width: auto; /* Adjusted width */
        background-color: darkgreen;
        color: white;
        border: 4px solid #8B4513; /* Set dark brown border */
        border-radius: 10px;
        cursor: pointer;
    }

    button:hover {
        background-color: green;
    }
</style>


