<script>

</script>

<section id="intro" class="frame mt-8">
    <div class="section-content flex flex-col items-center lg:flex-row">
        <div class="intro-left flex flex-col items-center text-center order-2 lg:order-1 lg:text-left lg:items-start">
            <div class="intro-text py-2 flex flex-col items-center lg:items-start">
                <div class="header text-3xl 2xl:text-5xl">
                    <div>Hi, my <br>name is <b class="author">Saran<span class="dot text-orange-500 text-3xl ml-0.5">.</span></b></div>
                </div>
                <div class="description py-6 flex flex-col text-1xl 2xl:text-2xl">
                    <div class="first flex flex-col sm:flex-row">
                        <div class="profession">I'm a <b class="job-title">data analyst</b> from </div>
                        <div class="district sm:pl-1 lg:pl-0">Kanniyakumari,</div>
                    </div>
                    <div class="second">
                        <span class="state">Tamil Nadu.</span>
                    </div>  
                </div>
            </div>
            <div class="intro-button">
                <button class="main-button">
                    <span>Contact Me</span>
                </button>
            </div>
        </div>
        <div class="intro-right order-1 lg:order-2">
            <div class="intro-image mx-8 mt-1.5 mb-4 w-[260px] md:w-[300px]">
                <img src="images/intro-image-320.png" alt="" srcset="">
            </div>
        </div>
    </div>
</section>

<style>
    .intro-left { width: 620px; }
    .intro-image { 
        /* width: 320px;  */
        filter: drop-shadow(-3px 17px 8px rgba(0, 0, 0, 0.3));
    }
    #intro .job-title {
        background-image: linear-gradient(135deg, rgb(255, 140, 5) 0%, rgb(214, 26, 94) 100%);
        background-clip: text;
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
    }
</style>