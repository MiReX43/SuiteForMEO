<nav>
    <div class="nav-container">
    <a href="/" class="nav-logo" title="Back to Homepage">MirFilms</a>
    <div class="nav-links">
        {#each nav as link}

        {#if link.isShow}
        <a href={link.href} class="link">{link.title}</a>
        {/if}
        
        {/each}
    </div>
    </div>
</nav>


    <div class="container">
    <!-- Pages will be injected below -->
    <slot></slot>
    </div>

    <script>
    const nav = [
        {
            title: 'Главная',
            href: '/',
            isShow: true,
        },
        {
            title: 'Фильмы',
            href: '/blog',
            isShow: true,
        },
        {
            title: 'Портфолио',
            href: '/project',
            isShow: false,
        },
        {
            title: 'Контакты',
            href: '/contact',
            isShow: false,
        },
        {
            title: 'temp',
            href: '/temp',
            isShow: false,
        },
    ]
    </script>



<style>
    .container {
    max-width: 1400px;
    margin: 50px auto;
    }
    
</style>