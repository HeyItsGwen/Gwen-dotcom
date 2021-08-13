<script>
    window.addEventListener('load',e=>{
        window.$('.carousel').on('slid.bs.carousel', function () {
            console.log(window.$('#zero')[0].classList);
            //get all slide elements
            let slide0 = window.$('.zero')[0];
            let slide1 = window.$('.one')[0];
            let slide2 = window.$('.two')[0];
            let slide3 = window.$('.three')[0];
            let slide4 = window.$('.four')[0];

            //array to iterate through slides to check which is active
            let slidesToCheck = [slide0,slide1,slide2,slide3,slide4];
            //check if each slide has an 'active' class
            for(let i=0;i<slidesToCheck.length;i++) {
                //if it does, show the correlating p element
                if(!slidesToCheck[i].classList.contains('active')){
                    window.$(`.carousel${i}`)[0].classList.remove('d-flex');
                    window.$(`.carousel${i}`)[0].classList.add('d-none');

                    window.$(`.carousel${i}p`)[0].classList.remove('d-flex');
                    window.$(`.carousel${i}p`)[0].classList.add('d-none');

                    window.$(`.carousel${i}p2`)[0].classList.remove('d-flex');
                    window.$(`.carousel${i}p2`)[0].classList.add('d-none');

                    window.$(`.carousel${i}p3`)[0].classList.remove('d-flex');
                    window.$(`.carousel${i}p3`)[0].classList.add('d-none');
                } else {
                    //otherwise make sure it's hidden
                    window.$(`.carousel${i}`)[0].classList.remove('d-none');
                    window.$(`.carousel${i}`)[0].classList.add('d-flex');

                    window.$(`.carousel${i}p`)[0].classList.remove('d-none');
                    window.$(`.carousel${i}p`)[0].classList.add('d-flex');

                    window.$(`.carousel${i}p2`)[0].classList.remove('d-none');
                    window.$(`.carousel${i}p2`)[0].classList.add('d-flex');

                    window.$(`.carousel${i}p3`)[0].classList.remove('d-none');
                    window.$(`.carousel${i}p3`)[0].classList.add('d-flex');
                }
            }
        })
    });
</script>

<div class='container d-flex flex-column '>
    <h2 class='align-self-center'>- Projects -</h2>
    <div class='d-flex flex-column flex-md-row' id='projects'>
        <div class='carouselText order-1 order-md-0 flex-column'>
            <h3 class='d-flex carousel0'>Frenchtown Deli and Catering</h3>
            <p class='justify-self-start carousel0p d-flex carouselTextLinks'>Project GitHub:&nbsp;<a href='https://github.com/HeyItsGwen/Frenchtown-Deli-and-Catering' target='blank'>click here!</a></p>
            <p class='justify-self-start carousel0p2 d-flex carouselTextLinks'>Project Website:&nbsp;<a href='https://heyitsgwen.github.io/Frenchtown-Deli-and-Catering/' target='blank'>click here!</a></p>

            <p class='carousel0p3 d-flex text-wrap text-right carouselTextDescription'>This site was created as a redesign for a local (to me) restaurant who's website was outdated and deprecated. It's a static single page site made entirely with vanilla js, bootstrap, and sass. The different "pages" on the site work similarly to react, but don't rely on components/frameworks to do the heavy lifting.</p>

            <h3 class='d-none carousel4'>The Lil' Gauntlet</h3>
            <p class='justify-self-start carousel4p d-none carouselTextLinks'>Project GitHub:&nbsp;<a href='https://github.com/HeyItsGwen/The-Lil-Gauntlet' target='blank'>click here!</a></p>
            <p class='justify-self-start carousel4p2  d-none carouselTextLinks'>Project Website:&nbsp;<a href='https://heyitsgwen.github.io/The-Lil-Gauntlet/' target='blank'>click here!</a></p>

            <p class='justify-self-end carousel4p3 d-none text-right text-wrap carouselTextDescription'>This site is a simple 2d browser based version of The Gauntlet from the game Oldschool Runescape. It's built entirely with vanilla javascript and bootstrap, and includes an inventory system, and item creation system, and a basic walk/pathing algorithm.</p>

            <h3 class='d-none carousel1'>Abstract</h3>
            <p class='justify-self-start carousel1p d-none carouselTextLinks'>Project GitHub:&nbsp;<a href='https://github.com/HeyItsGwen/Abstract-Landing' target='blank'>click here!</a></p>
            <p class='justify-self-start carousel1p2 d-none carouselTextLinks'>Project Website:&nbsp;<a href='https://heyitsgwen.github.io/Abstract-Landing/' target='blank'>click here!</a></p>

            <p class='justify-self-end carousel1p3 d-none text-right text-wrap carouselTextDescription'>This static site was created to be a sample company/product landing page, and for me to have a little fun with some abstract/asymetrical design ideas, as well as to get some experience with React. It was built with React and Bootstrap.</p>

            <h3 class='d-none carousel3'>Oldschool Runescape Landing Page</h3>
            <p class='justify-self-start carousel3p d-none carouselTextLinks'>Project GitHub:&nbsp;<a href='https://github.com/HeyItsGwen/OSRS-Landing-Page' target='blank'>click here!</a></p>
            <p class='justify-self-start carousel3p2  d-none carouselTextLinks'>Project Website:&nbsp;<a href='https://heyitsgwen.github.io/OSRS-Landing-Page/' target='blank'>click here!</a></p>

            <p class='justify-self-end carousel3p3 d-none text-right text-wrap carouselTextDescription'>This single page site was built to be an example of a landing page for the game Oldschool Runescape. It's built using existing art assets from other sites under the game's umbrella, and was built with plain HTML, Bootstrap, and Sass.</p>

            <h3 class='d-none carousel2'>Brand Spotlight</h3>
            <p class='justify-self-start carousel2p d-none carouselTextLinks'>Project GitHub:&nbsp;<a href='https://github.com/HeyItsGwen/Simple-Landing-Page' target='blank'>click here!</a></p>
            <p class='justify-self-start carousel2p2  d-none carouselTextLinks'>Project Website:&nbsp;<a href='https://heyitsgwen.github.io/Simple-Landing-Page/' target='blank'>click here!</a></p>

            <p class='justify-self-end carousel2p3 d-none text-right text-wrap carouselTextDescription'>This static site was designed to be an example of a more minimalist/material design for a product or company's landing page. It was built using React and Bootstrap, mainly to get a little practice with React and some more simple designs.</p>

        </div>
        <div id="carousel" class="carousel slide order-0 order-md-1" data-ride="carousel">
            <ol class="carousel-indicators">
              <li data-target="#carousel" data-slide-to="0" class="active"></li>
              <li data-target="#carousel" data-slide-to="1"></li>
              <li data-target="#carousel" data-slide-to="2"></li>
              <li data-target="#carousel" data-slide-to="3"></li>
              <li data-target="#carousel" data-slide-to="4"></li>
            </ol>
            <div class="carousel-inner">
              <div id='zero' class="zero carousel-item active">
                <img src="./images/frenchtown.png" class="d-block w-100" alt="frenchtown deli and catering redesign">
              </div>
              <div class="one carousel-item">
                <img src="./images/abstract.png" class="d-block w-100" alt="a colorful and abstract product/company landing page">
              </div>
              <div class="two carousel-item">
                <img src="./images/brandspotlight.png" class="d-block w-100" alt="a simple minimalist brand spotlight page">
              </div>
              <div class="three carousel-item">
                <img src="./images/osrs.png" class="d-block w-100" alt="an oldschool runescape landing page">
              </div>
              <div class="four carousel-item">
                <img src="./images/lilgauntlet.png" class="d-block w-100" alt="a web recreation of a minigame from oldschool runescape (the gauntlet)">
              </div>
            </div>
            <a class="carousel-control-prev" href="#carousel" role="button" data-slide="prev">
              <span class="carousel-control-prev-icon" aria-hidden="true"></span>
              <span class="sr-only">Previous</span>
            </a>
            <a class="carousel-control-next" href="#carousel" role="button" data-slide="next">
              <span class="carousel-control-next-icon" aria-hidden="true"></span>
              <span class="sr-only">Next</span>
            </a>
          </div>
    </div>
</div>

<style>
    .container {
        width: 100%;
        max-width: 1000px;
        margin: 50px auto;
    }
    div{
        width: 100%;
    }
    h2{
		font-size: 1.3em;
        margin-bottom: 30px;
	  }
    h3{
      font-size: 1.1em;
    }
    .carousel {
        width: 100%;
        margin: auto;
        border-radius: 5px;
        overflow: hidden;
    }
    .carouselText {
      width: 100%;
      padding: 35px 35px 0 35px;
    }
    .carouselTextLinks{
      margin-bottom: 0;
      font-size: 0.9em;
    }
    .carouselTextLinks a {
      color: rgb(202, 127, 139);
    }
    .carouselTextDescription{
      margin-top: 15px;
    }
</style>