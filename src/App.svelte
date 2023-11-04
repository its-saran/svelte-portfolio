<script>
    import Navbar from "./lib/Navbar.svelte";
    import MobileMenu from "./lib/mobileMenu.svelte";
    import Intro from "./lib/Intro.svelte";
    import About from "./lib/About.svelte";
    import Skills from "./lib/Skills.svelte";
    import Portfolio from "./lib/Porfolio.svelte";
    import Qualifications from "./lib/Qualifications.svelte";
    import Contact from "./lib/Contact.svelte";
    import Copyright from "./lib/Copyright.svelte";

    // import { onMount } from 'svelte';

    // let isFixed = false;
    // const handleScroll = () => {
    //     isFixed = window.scrollY > 70;
    // };

    // // Add scroll event listener when the component is mounted
    // onMount(() => {
    //     window.addEventListener('scroll', handleScroll);
    //     return () => {
    //         window.removeEventListener('scroll', handleScroll);
    //     };
    // });

</script>


<!-- 
<header class:fixed={isFixed}> -->
<header>
    <Navbar/>
    <!-- <MobileMenu/> -->
</header>
<main>
    <Intro/>
    <!-- 
    <About/>
    <Skills/>
    <Portfolio/>
    <Qualifications/>
    <Contact/> -->
</main>
<footer>
    <!-- <Copyright/> -->
</footer>

<style>
</style>


