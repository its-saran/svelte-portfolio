<script>
    import Navbar from "./lib/Navbar.svelte";
    import Intro from "./lib/Intro.svelte";
    import About from "./lib/About.svelte";
    import Skills from "./lib/Skills.svelte";
    import Portfolio from "./lib/Porfolio.svelte";
    import Qualifications from "./lib/Qualifications.svelte";
    import Contact from "./lib/Contact.svelte";
    import Copyright from "./lib/Copyright.svelte";
</script>

<header>
    <Navbar/>
</header>
<main>
    <Intro/>
    <About/>
    <Skills/>
    <Portfolio/>
    <Qualifications/>
    <Contact/>
</main>
<footer>
    <Copyright/>
</footer>

