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
            <img src={page.image} alt="Image" />
            <div class="post-content">
                <h3>{page.title}</h3>
                <p><b>Год выпуска: </b>{page.st1}</p>
                <p><b>Страна: </b>{page.st2}</p>
                <p><b>Жанр: </b>{page.st3}</p>
                <p><b>Продолжительность: </b>{page.st4}</p>
                <p><b>Режиссер: </b>{page.st5}</p>
                <p><b>Актеры: </b>{page.st6}</p>
                <p>{page.body}</p>
            </div>
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
    width: 70%;
    height: 100%vh;
    margin: 5px auto;
    }

    .blogposts {
    display: grid;
    grid-template-columns: 1fr; 
    grid-gap: 30px;
    padding: 40px 20px;
    
    }
    .post {
    border: 0px solid #000000;
    padding: 20px;
    box-shadow: 0 0 10px #000000;
    text-align: left;
    display: grid;
    grid-template-columns: 1fr 100fr; 
    grid-gap: 20px;
    
    }

    .post img {
    display: block; /* Сделать изображение блочным элементом */
    margin: 0; /* Автоматическое выравнивание по горизонтали */
    height: 300px;
    width: 200px;
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