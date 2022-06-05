<template>
<main>
    <section>
        <div class="logo">
        <logo-image :source="'/onda-cero-logo.png'"/>
        </div>
        <h1>CONECTARSE</h1>
        <p style="text-align: center;">¿Todavía no tienes una cuenta? <nuxt-link to="/register"><span class="Link">RESGISTRATE</span></nuxt-link></p>
        <div class="icons"></div>
        <div class="form">
            <p class="white">Nombre de usuario o correo electrónico</p>
            <input type="email" name="Correo electrónico">
            <p class="white">Contraseña</p>
            <input type="password" name="Contraseña">
            <div class="options">
                <button><nuxt-link to="/page1">INICIAR SESIÓN</nuxt-link></button>
                <p style="color: #fff; text-align: center">¿HAS OLVIDADO TU CONTRASEÑA?</p>
                <p>O <span style="color: #fff; text-align: center"><nuxt-link to="/page1">¿PREFIERES ENTRAR SIN INICIAR SESIÓN?</nuxt-link></span></p>
            </div>
        </div>
    </section>
</main>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
