<template>
<main>
    <section>
        <div class="logo">
        <logo-image :source="'/onda-cero-logo.png'"/>
        </div>
        <h1>REGISTRARSE</h1>
        <div class="icons"></div>
        <div class="form">
            <p class="white">Nombre de usuario o correo electrónico</p>
            <input type="email" name="Correo electrónico">
            <p class="white">Contraseña</p>
            <input type="password" name="Contraseña">
            <p class="white">Repita la contraseña</p>
            <input type="password" name="Contraseña">
            <div class="options">
                <button><nuxt-link to="/page1">INICIAR SESIÓN</nuxt-link></button>
                <p style="text-align: center">¿YA TIENES UNA CUENTA? <span style="color: #fff;"><nuxt-link to="/">INICIA SESIÓN</nuxt-link></span></p>
                <p>O <span style="color: #fff; text-align: center"><nuxt-link to="/page1">¿PREFIERES ENTRAR SIN INICIAR SESIÓN?</nuxt-link></span></p>
            </div>
        </div>
    </section>
</main>
</template>

<script>
export default {
  name: 'RegisterPage'
}
</script>
