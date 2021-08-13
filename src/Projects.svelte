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

            //array to iterate through to check for what's active
            let slidesToCheck = [slide0,slide1,slide2,slide3,slide4];
            //check if each slide has an 'active' class
            for(let i=0;i<slidesToCheck.length;i++) {
                //if it does, show the correlating p element
                if(!slidesToCheck[i].classList.contains('active')){
                    window.$(`#carousel${i}`)[0].classList.remove('d-flex');
                    window.$(`#carousel${i}`)[0].classList.add('d-none');
                } else {
                    //otherwise make sure it's hidden
                    window.$(`#carousel${i}`)[0].classList.remove('d-none');
                    window.$(`#carousel${i}`)[0].classList.add('d-flex');
                }
            }
        })
    });
</script>

<div class='container d-flex flex-column '>
    <h2 class='align-self-center align-self-md-end'>- Projects -</h2>
    <div class='d-flex flex-column flex-md-row' id='projects'>
        <div class='carouselText order-1 order-md-0'>
            <p id='carousel0' class='d-flex'>Frenchtown</p>
            <p id='carousel1' class='d-none'>Abstract</p>
            <p id='carousel2' class='d-none'>Brand Spotlight</p>
            <p id='carousel3' class='d-none'>Oldschool Runescape</p>
            <p id='carousel4' class='d-none'>The Lil' Gauntlet</p>
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
        margin-bottom: 20px;
	}
    .carousel {
        width: 100%;
        margin: auto;
    }
</style>