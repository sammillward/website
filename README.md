
<html>
    <head>
        <title>Sam's Resume</title>
      
        <!-- stylesheet -->
        <link rel="stylesheet" href="./style.css"/>
    </head>
    <body>
        <div class="container">
          <h1>My Resume</h1>
          <p>My name is Sam Millward. I am a student at BYU, currently I am in the pre business program, and I am planning on studying accounting when I finish all of the prerequisites. I had previously studied at BYU Hawaii before I transferred to BYU Provo. As well as studying here at BYU, I also work part time at Chick-Fil-A. Here is a little bit more about me below.</p>
        </div>
      <ol>
      1. Educational History
      <ul>
      <li>Graduated Boise High School class of 2020</li>
      <li>Studied at BYU Hawaii (from Fall 2020 through June 2023, with a 2 year break from 2021 through 2022, during which time I was a volunteer representative for The Church of Jesus Christ of Latter Day Saints</li>
      <li>Current student at BYU</li>
      </ul>
      2. Employment History
      <ul>
      <li>Cashier at Carls Jr (May 2019 - June 2019, April 2020 - June 2020)</li>
      <li>Paint Associate at Home Depot (July 2020 - October 2020)</li>
      <li>Worked at Chick-Fil-A (July 2023 - November 2024)</li>
      </ul>
      3. Volunteer Activities
      <ul>
      <li>Eagle Scout project in 2016 - set up signs at a reserve informing people about an endangered species of bird and asking them not to shoot them</li>
      <li>Spent almost 2 years (from January 2021-December 2022) as a volunteer              representative for The Church of Jesus Christ of Latter Day Saints</li>
      </ul>
      </ol>
    <a href="http://127.0.0.1:5500/myfinalproject.html">A bit more about me here </a>

<!-- Embed Code for YouTube Video Player with Plyr -->
<div id="player-container" style="max-width: 1000px; margin: 0 auto;"></div>

<script>
(function() {
    function initPlyrPlayer(videoId, containerId) {
        if (!document.getElementById(containerId)) {
            console.error(`Container with id "${containerId}" not found.`);
            return;
        }

        if (!document.querySelector('link[href="https://cdn.plyr.io/3.7.2/plyr.css"]')) {
            const plyrCSS = document.createElement('link');
            plyrCSS.rel = 'stylesheet';
            plyrCSS.href = 'https://cdn.plyr.io/3.7.2/plyr.css';
            document.head.appendChild(plyrCSS);
        }

        if (!document.querySelector('script[src="https://cdn.plyr.io/3.7.2/plyr.js"]')) {
            const plyrScript = document.createElement('script');
            plyrScript.src = 'https://cdn.plyr.io/3.7.2/plyr.js';
            document.body.appendChild(plyrScript);
            plyrScript.onload = () => setupPlayer(videoId, containerId);
        } else {
            setupPlayer(videoId, containerId);
        }
    }

    function setupPlayer(videoId, containerId) {
        const container = document.getElementById(containerId);
        container.innerHTML = `
            <div class="plyr__video-embed" id="player">
                <iframe src="https://www.youtube.com/embed/${videoId}?rel=0&showinfo=0&modestbranding=1&enablejsapi=1&origin=*&playlist=${videoId}&loop=1&iv_load_policy=3"
                        allowfullscreen
                        allow="autoplay; encrypted-media">
                </iframe>
            </div>
        `;

        const style = document.createElement('style');
        style.textContent = `
            #${containerId} .plyr__video-embed iframe {
                aspect-ratio: 16 / 9;
                width: 100%;
            }
            #${containerId} .plyr__video-embed iframe {
                pointer-events: none;
            }
        `;
        document.head.appendChild(style);

        new Plyr(`#${containerId} .plyr__video-embed`, {
            youtube: {
                noCookie: true,
                rel: 0,           
                showinfo: 0,     
                iv_load_policy: 3,
                modestbranding: 1 
            }
        });
    }

    document.addEventListener('DOMContentLoaded', () => {
        initPlyrPlayer('iadzYtX4ERU', 'player-container');
    });
})();
</script>
    
    </body>
</html>
