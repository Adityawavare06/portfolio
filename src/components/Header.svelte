<script>
    export let y;

    export let tabs = [
        { name: "Projects ", link: "#projects" },
        { name: "About me", link: "#about" },
        { name: "Blog", link: "https://www.youtube.com/shorts/9DOo_UqC310" },
        //  { name: "Contact", link: "#Contact" },
        // {name: '', link: ''},
    ];
   
    function gobottom() {
  const footer = document.getElementById("footer"); // Get the footer element
  footer.scrollIntoView({
    behavior: 'smooth',  // Smooth scroll effect
    block: 'start'       // Align the top of the footer with the top of the viewport
  });
}   

</script>

<header
    class={"sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border-b border-solid " +
        (y > 0
            ? " py-4 bg-slate-950 border-violet-950"
            : " py-6 bg-transparent border-transparent")}
>
    <h1 class="font-medium">
     <a href="/" >   <b class="font-bold poppins">Aditya </b> <span class="">wavare</span> </a>
    </h1>
    <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as tab, index}
            <a
                href={tab.link}
                class="duration-200 hover:text-violet-400"
                target={index === 2 ? "_blank" : ""}
            >
                <p>{tab.name}</p>
            </a>
        {/each}
        <!-- <button
            class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-violet-600 text-white"
        >
            <div
                class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
            />
            <h4 class="relative z-9">Login</h4>
        </button> -->
        <button  on:click={gobottom}
            class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950"
        >
            <!-- <div
                class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
            /> -->
          <a href="#Contact"><h4 class="relative z-9">Get in touch</h4></a>
            
        </button>
    </div>
</header>
