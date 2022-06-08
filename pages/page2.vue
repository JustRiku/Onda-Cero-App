<template>
    <body>
        <nav-bar class="nav-bar"/>
        <main class="main-page2">
            <section class="profile">
                <div class="profile-pic"><img :src="'/Vector.png'" alt=""></div>
                <h2 class="profile-name">Nombre perfil</h2>
            </section>
            <article>
                <nav>
                    <ul class="list-bar" style="display: flex; list-style: none;">
                        <li class="selected">Favoritos</li>
                        <li>Escuchar más tarde</li>
                        <li>Playlist</li>
                    </ul>
                </nav>
            </article>
            <section class="list-podcast">
                <h2 class="number-podcast">O podcasts favoritos</h2>
                <div class="list-content">
                    <h3>Aún no has añadido ningun podcast</h3>
                    <p>Busca algún podcast para añadirlo aquí.</p>
                    <button class="green-button">Añadir podcast</button>
                    </div>
            </section>
        </main>
    </body>
</template>