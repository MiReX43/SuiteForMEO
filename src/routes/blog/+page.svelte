<svelte:head>
    <title>Блoг</title>
</svelte:head>

<div class='container'>
    <div class='info'>
        <div class='animate-background'>
            <div class='container info-container'>
                <div class='info-text'>
                    <h1>
                        <p class='animate-text-1'>Каталог</p>
                    </h1>
                </div>
  
            </div>
        </div>
    </div>
</div>

<div class='background-div'>
<div class="blogposts">
    {#each routes as page} 
        <div class="post"> 
            <h2>{page.title}</h2>
            <p>{page.body}</p>
            <p class="readmore">
                <a class="link" href={`/blog/posts/${page.id}`}>
                    Читать далее
                </a>
            </p>
        </div>
    {/each}
</div>

</div>


<script>
    import {routes} from './routes'
</script>

<style>
    .container {
    max-width: 1400px;
    margin: 50px 0 0 2.5rem;
    }

    .background-div {
    background-color: #999999;
    width: 100%;
    height: 57vh;
    margin: 5px auto;
    }

    .blogposts {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr; 
    grid-gap: 20px;
    padding: 76px 20px;
    }
    .post {
    border: 0px solid #000000;
    padding: 10px;
    box-shadow: 0 0 10px #000000;
    }
    .link {
    color: rgb(255, 255, 255);
    }

    .info {
    text-align: center;
    position: relative;
    }
    .info-container {
    height: 100%; 
    display: flex;
    flex-direction: column;
    justify-content: center; 
    text-align: left;
    align-items: start;
    }

    .info h1 {
    font-size: 4rem;
    margin: 0;
    }
    .info h1 p { 
    position: relative;
    font: inherit;
    margin: 0;
    text-align: left; 
    line-height: 130%; 
    width: fit-content;
    font-weight: 800; 
    letter-spacing: -0.03em;
    }

    .info .info-text {
    position: relative;
    }

    .animate-text-1 {
        color: white;
    }

    .info-text {
        position: fixed;
    }
    .scroll-button { 
    display: flex;
    border: none;
    outline: none;
    cursor: pointer;
    }
    .scroll-button .arrow {
    margin-left: 0.50rem;
    }
</style>