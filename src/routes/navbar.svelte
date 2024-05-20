<script>
    import { slide } from 'svelte/transition'; 
    import { cubicInOut } from 'svelte/easing'; 

    let menu = false;
    let acorn; 
    let i = 0; 

    function toggleMenu() {
        i ++; 
        if (i > 0) {
            menu = true; 
            acorn.style.transform = "rotate(90deg)"; 
        } if ( i > 1) {
            menu = false; 
            i = 0; 
            acorn.style.transform = "rotate(0deg)"; 
        }
    }
    
</script>

<div class="nav-wrapper">
    <div class="nav-content">
        <h3 class="logo-title">A Texan's Life</h3>
        <ul>
            <li><a href="/">Home</a></li>
            <li><a href="/biography">Biography</a></li>
            <li><a href="/about">About</a></li>
        </ul>
        <button class="acorn" on:click={toggleMenu} bind:this={acorn}>☰</button>
    </div>

    {#if menu === true}
        <div class="menu" transition:slide={{duration: 500, easing: cubicInOut}}>
            <button class="xmark" on:click={toggleMenu}>✕</button>
            <a href="/" on:click={toggleMenu}>Home</a>
            <a href="/early-years" on:click={toggleMenu}>Early Years</a>
            <a href="/adulthood" on:click={toggleMenu}>Adulthood</a>
            <a href="/later-years" on:click={toggleMenu}>Later Years</a>
            <a href="/biography" on:click={toggleMenu}>Biography</a>
            <a href="/about" on:click={toggleMenu}>About</a>
        </div>
    {/if}
</div>

<style>

    button {
        border: none; 
        background-color: transparent;
        color: black;
    }

    .nav-wrapper {
        background-color: #ffffff;
        height: 50px;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: row;
        position: fixed;
        z-index: 100;
        margin: 0;
        box-shadow: 0px 1px 10px rgba(0, 0, 0, 0.1);
        z-index: 999;
    }

    .nav-content {
        display: flex;
        flex-direction: row;
        align-items: center;
        width: 80%;
        max-width: 1000px;
        justify-content: space-between;
    }

    .nav-content h3 {
        font-weight: 400;
        font-size: 0.9rem;
        color: var(--secondary-color);
    }

    ul {
        list-style: none;
        display: flex;
        flex-direction: row;
        gap: 30px;
        padding: 0;
    }

    li {
        display: flex;
        font-family: "Inter";
        font-weight: 500;
        font-size: 1rem;
    }

    a {
        color: #000000;
        font-weight: 400;
        font-size: 0.9rem;
        opacity: 50%;
        transition: opacity 0.4s ease;
    }

    .logo-title {
        display: flex;
        font-size: 0.9rem;
    }

    .acorn {
        display: none;
    }

    @media all and (min-width: 701px) {
        a:hover {
            opacity: 100%;
            transition: opacity 0.4s ease;
        }
    }

    @media all and (max-width: 700px) {
        .nav-wrapper {
            align-items: center;
            justify-content: center;
        }

        .nav-content {
            justify-content: center;
            width: 100%;
            position: relative;
        }

        .acorn {
            display: flex;
            flex-direction: column;
            height: 30px;
            width: 30px;
            position: absolute;
            right: 20px;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            transition: transform .4s ease;
        }

        .logo-title {
            position: absolute;
            left: 20px;
        }

        ul {
            display: none;
            gap: 30px;
            justify-content: center;
            padding: 0;
            margin: 0;
        }

        li {
            font-weight: 600;
        }

        a {
            opacity: 100%;
        }

        li:hover a {
            color: #2f1f00;
            transition: color 0.2s;
        }

        
    }

    .menu {
        display: flex;
        flex-direction: column;
        height: 500px;
        width: 90%;
        -webkit-backdrop-filter: blur(20px);
        backdrop-filter: blur(50px);
        background-color: rgba(255, 255, 255, 1);
        position: fixed;
        z-index: 999;
        border-radius: 20px;
        top: 100px;
        border: 1px solid var(--accent-color); 
        align-items: center;
        justify-content: space-evenly;
    }

    .menu a {
        font-size: 1.5rem; ;
    }

    .xmark {
        display: flex; 
        position: absolute;
        align-items: center;
        justify-content: center; 
        height: 30px; 
        width: 30px; 
        top: 10px;
        right: 10px; 
        font-size: 1.8rem;
    }



</style>
