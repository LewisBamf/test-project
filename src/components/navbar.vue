<template>
    <div class="navbar">
        <svg view-box="50px 50px">
          <image :href="require('@/assets/logo.svg')" alt="logo" class="logo"/>
        </svg>

    <div class="nav-links">
        <h2>home</h2>
        <h2>pricing</h2>
        <h2>contact</h2>
        <h2>about us</h2>
    </div>

    </div>

</template>

<!-- script stuff here -->
<script>

export default{
    name: "nav-bar"
}
</script>


<style>

.navbar{
    height: 40px;
    width: 100vw;
    margin: 0px;
    padding-top: 8px;
    padding-bottom: 8px;
    padding-left: 1em;
    padding-right: 1em;
    position: fixed;
    top: 0;
    left: 0;
    display: flex;
    flex-direction: row;
    overflow: hidden;
    background-color: var(--background);
    box-shadow: 0px 0px 6px var(--text);
    z-index: 1000;
    justify-content: space-between;
}

.logo{
    height: 100%;
    z-index: 2000;
    background-color: transparent;
    fill: var(--primary);
}

.nav-links{
    justify-content: space-around;
    gap: 20px;
    align-items: center;
    width: fit-content;
    text-wrap: nowrap;
    height: 100%;
    display: flex;
    flex-direction: row;
    margin-left: 0%;
    margin-right: 5%;
    background-color: transparent;
    z-index: 1001;
}

h2{
    color: var(--text);
    transition: opacity 0.3s ease;
}

h2:hover{
    opacity: 0.6;
    cursor: pointer;
}
</style>