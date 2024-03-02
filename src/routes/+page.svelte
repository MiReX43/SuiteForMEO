<svelte:head>
    <title>MirFilms</title>
</svelte:head>

<div class='container'>
    <div class='info'>
        <div class='animate-background'>
            <div class='container info-container'>
                <div class='info-text'>
                    <h1>
                        <p class='animate-text-1'>Только лучшие филмы</p>
                        <p class='text-2'>В нашем кинотиатре</p>
                    </h1>
                </div>
                <h2 class='subtitle'>
                    "Добро пожаловать в наш кинотеатр! Насладитесь неповторимой атмосферой кинематографа в самом сердце города. Откройте для себя широкий выбор фильмов различных жанров: от захватывающих блокбастеров до утонченных инди-произведений. Наши современные кинозалы оснащены передовой звуковой и видео техникой, чтобы каждый просмотр стал незабываемым событием. Приходите вместе с друзьями или семьей и окунитесь в мир киноискусства вместе с нами!"                </h2>
                <div style='color:black' class='scroll-button animate-scroll' tabindex="0">
                    <a href='/blogg'>Сейчас в кино</a>
                    <div class='arrow'>→</div>
                </div>
            </div>
        </div>
    </div>
</div>
<div class='background-div'></div>



<style> .info {
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
    .container {
    max-width: 1400px;
    margin: 50px 0 0 2.5rem;
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
    .info h2 {
    max-width: 65ch;
    font-weight: 200; 
    margin-top: 0.50rem;
    }
    .background-div {
    background-color: #999999;
    width: 100%;
    height: 57vh;
    margin: -320px auto;
    }
    .info .info-text {
    position: relative;
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

    .animate-text-1 {
        color: white;
    }
    .text-2 {
        color: white;
    }
    </style>