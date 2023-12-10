<style>
.nav-wrapper {
    background-color: rgba(255, 252, 246, 0.7);
    -webkit-backdrop-filter: blur(10px);
    backdrop-filter: blur(10px);    
    height: 60px;
    width: 100vw; 
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: row;
    gap: 45vw;
    position: fixed; 
    z-index: 100;
    margin: 0;
}

ul {
    list-style: none;
    display: flex;
    flex-direction: row;
    gap: 1vw;
    padding: 0;
}

li {
    display: flex;
    font-family: 'Plus Jakarta Sans'; 
    font-weight: 400;
    font-size: 1rem;
    padding: 10px 10px;
    border-radius: 16px;
    transition: background-color 0.5s, color 0.5s, border 0.3s;
    border: 1px solid transparent;

}

li:hover {
    display: flex;
    border: 1px solid #2f1f00;
    cursor: pointer;
    transition: background-color 0.5s, color 0.5s, border 0.3s;
}

a {
    transition: background-color 0.5s, color 0.5s, border 0.3s;
}

li:hover a {
    color: #2f1f00; 
    transition: color 0.2s; 
}

.logo-title {
        display: flex; 
}

@media all and (max-width: 700px) {
    .nav-wrapper {
        align-items: center;
        justify-content: center;
        -webkit-backdrop-filter: blur(10px);
        backdrop-filter: blur(10px);
    }

    .logo-title {
        display: none; 
    }

    ul {
        gap: 8vw;  
        justify-content: center;
        padding: 0;
        margin: 0; 
    }

    li {
        font-weight: 600;
    }
}

</style>


<div class="nav-wrapper">
    <h3 class="logo-title">A Texan's Life</h3>
    <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/explore">Explore</a></li>
        <li><a href="/biography">Biography</a></li>
    </ul>
</div>
