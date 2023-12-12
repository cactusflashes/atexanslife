<script>
    import juanChild from '/src/lib/vis/jp-child.png'
    import juanAdult from '/src/lib/vis/juan-adult.png'
    import juanGuitarBW from '/src/lib/vis/jp-guitar-bw.png'
    import texan from '/src/lib/vis/texan-bw.png'

    function navigate() {
        window.location.href =""; 
    }


</script>
<div class="container">    
    <div class="mobile-spacer"></div>    
    <h2 style="width: 75%; font-size: 2.5rem;">Explore the life of Juan Peréz.</h2>
    <div class="vert-row-col">
        <div class="row-contain">
            <a class="item-listing" href="/early-years">
                <h3 class="item-listing-header">Early years & adolescence</h3>
                <h4 class="years"> 1945 - 1962</h4>
                <img src={juanChild} alt="Juan Perez as a child." class="small-img">
            </a>
            <a class="item-listing" href="/adulthood">
                <h3 class="item-listing-header-right">Adulthood</h3>
                <h4 class="years-right"> 1962 - 2011</h4>
                <img src={juanAdult} alt="Juan Perez as an adult." class="small-img-left">
            </a>
            <a class="item-listing" href="/later-years">
                <h3 class="item-listing-header">Later years & family</h3>
                <h4 class="years"> 2011 - 2023</h4>
                <img src={juanGuitarBW} alt="Juan Perez as an older man." class="med-img">
            </a>
        </div>
            <a class="bottom-item-listing" href="/biography">
                <h3  style="width: 50%; text-align: right; " class="item-listing-header-right">Read A Texan's Life at a Glance</h3>
                <h4 class="years-right"> 2015 - 16</h4>
                <img src={texan} alt="A hand holding a biography." class="med-img-left">
            </a>
    </div>
    <div class="spacer"></div>
    <div class="spacer"></div>

</div>