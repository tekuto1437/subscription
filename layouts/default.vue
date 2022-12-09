<script>
// Use same logic for routing, name of route must be exact same as file name
// And all of links must be wrapped in nuxt-link tag
// Do not copy my styles of my navbar, it's just for preview
</script>

<template>
    <div class="toReplace" >Navbar goes here instead
        <ul class="list">

            <nuxt-link to="/">
                <li>Subscription</li>
            </nuxt-link>

            <nuxt-link to="aboutUs">
                <li class="link">About us</li>
            </nuxt-link>

            <nuxt-link to="admin-page">
                <li class="link">Admin page</li>
            </nuxt-link>

            <nuxt-link to="CONTACTus">
                <li class="link">Contact us</li>
            </nuxt-link>

        </ul>
    </div>
    <NuxtLoadingIndicator />
    <NuxtPage/>
</template>

<style>
*, *::after, *::before {
    box-sizing: border-box;
}

html, body {
    margin: 0;
    padding: 0;
    width: 100%;
    height: 100%;
}

.toReplace {
    width: 100%;
    height: 30px;
    background-color: #484C54;
    display: flex;
    justify-content: center;
    align-items: center;
}

.list {
    display: flex;
    list-style-type: none;
}

.link {
    margin: 0 10px;
}

</style>