<script>
    import downloadLogo from '/images/download-dark.svg';

    // Tailwind class
    let navbar = "navbar overflow-hidden z-10 py-2 px-2 md:px-6"
    let logoText = "btn btn-ghost normal-case text-4xl font-bold"
    let menu = "menu menu-horizontal"
    let menuItem = "transition-none rounded-md"
    let downloadButton = "main-button download-resume mr-4 hidden 2xl:flex"
    let themeSwitch = "swap swap-rotate mr-1.5 md:mr-4 lg:mr-6 2xl:mr-8"
    let menuSwitch = "btn btn-circle btn-ghost swap swap-rotate 2xl:hidden" 
    let navbarCenter = "navbar-center hidden 2xl:flex"
  
    let pageWidth = window.innerWidth;
    const handleResize = () => { pageWidth = window.innerWidth };

    let isLightTheme = false;
    const toggleTheme = () => { isLightTheme = !isLightTheme;};

    $: {
        const theme = isLightTheme ? 'light' : 'dark';
        document.documentElement.setAttribute('data-theme', theme);
    }


</script>
  
<svelte:window on:resize={handleResize} />
<nav id="navbar" class="{navbar}">
    <div class="navbar-start">
        <a id="logo-text" class="{logoText}">SARAN</a>
    </div>
    <div class="{navbarCenter}">
        <ul class="{menu}">
            <li><a href="#intro" class="{menuItem}">Home</a></li>
            <li><a href="#about" class="{menuItem}">About</a></li>
            <li><a href="#skills" class="{menuItem}">Skills</a></li>
            <li><a href="#portfolio" class="{menuItem}">Portfolio</a></li>
            <li><a href="#qualifications" class="{menuItem}">Experience</a></li>
            <li><a href="#contact" class="{menuItem}">Contact</a></li>
        </ul>
    </div>

    <div class="navbar-end">
        <label id="theme-switch" class="{themeSwitch}">
            <input type="checkbox" class="toggleTheme" on:change={toggleTheme} bind:checked={isLightTheme}/>
    
            <svg class="swap-on fill-current w-8 h-8" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M5.64,17l-.71.71a1,1,0,0,0,0,1.41,1,1,0,0,0,1.41,0l.71-.71A1,1,0,0,0,5.64,17ZM5,12a1,1,0,0,0-1-1H3a1,1,0,0,0,0,2H4A1,1,0,0,0,5,12Zm7-7a1,1,0,0,0,1-1V3a1,1,0,0,0-2,0V4A1,1,0,0,0,12,5ZM5.64,7.05a1,1,0,0,0,.7.29,1,1,0,0,0,.71-.29,1,1,0,0,0,0-1.41l-.71-.71A1,1,0,0,0,4.93,6.34Zm12,.29a1,1,0,0,0,.7-.29l.71-.71a1,1,0,1,0-1.41-1.41L17,5.64a1,1,0,0,0,0,1.41A1,1,0,0,0,17.66,7.34ZM21,11H20a1,1,0,0,0,0,2h1a1,1,0,0,0,0-2Zm-9,8a1,1,0,0,0-1,1v1a1,1,0,0,0,2,0V20A1,1,0,0,0,12,19ZM18.36,17A1,1,0,0,0,17,18.36l.71.71a1,1,0,0,0,1.41,0,1,1,0,0,0,0-1.41ZM12,6.5A5.5,5.5,0,1,0,17.5,12,5.51,5.51,0,0,0,12,6.5Zm0,9A3.5,3.5,0,1,1,15.5,12,3.5,3.5,0,0,1,12,15.5Z"/></svg>
            
            <svg class="swap-off fill-current w-8 h-8" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M21.64,13a1,1,0,0,0-1.05-.14,8.05,8.05,0,0,1-3.37.73A8.15,8.15,0,0,1,9.08,5.49a8.59,8.59,0,0,1,.25-2A1,1,0,0,0,8,2.36,10.14,10.14,0,1,0,22,14.05,1,1,0,0,0,21.64,13Zm-9.5,6.69A8.14,8.14,0,0,1,7.08,5.22v.27A10.15,10.15,0,0,0,17.22,15.63a9.79,9.79,0,0,0,2.1-.22A8.11,8.11,0,0,1,12.14,19.73Z"/></svg>
        </label>
    
        <button class="{downloadButton}">
            <svg xmlns="http://www.w3.org/2000/svg" width="25" height="25">
                <image xlink:href={downloadLogo} width="25" height="25"></image>
            </svg>
            <span>Resume</span>
        </button>
        
        <label id="menu-switch" class="{menuSwitch}">
            <input type="checkbox" class="toggleMenu"/>
    
            <svg class="swap-off fill-current" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 512 512"><path d="M64,384H448V341.33H64Zm0-106.67H448V234.67H64ZM64,128v42.67H448V128Z"/></svg>
            
            <svg class="swap-on fill-current" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 512 512"><polygon points="400 145.49 366.51 112 256 222.51 145.49 112 112 145.49 222.51 256 112 366.51 145.49 400 256 289.49 366.51 400 400 366.51 289.49 256 400 145.49"/></svg>
        </label>
    </div>
</nav>

<style>
    #logo-text {
        background-image: linear-gradient(135deg, rgb(255, 140, 5) 0%, rgb(214, 26, 94) 100%);
        background-clip: text;
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
    }
    #navbar .menu li { transition: margin 0.5s ease; }
    .menu a { letter-spacing: 1px; font-weight: 500; }
    .main-button:hover { background-position: right center; color: #1f2937; text-decoration: none; }
    .main-button:active { transform: scale(0.9); }
</style>
  
  
  