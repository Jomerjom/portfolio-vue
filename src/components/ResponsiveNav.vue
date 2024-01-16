<script setup>
</script>

<template>
    <nav class="navbar">
        <div class="navbar-container container">
            <input type="checkbox" name="" id="">
            <div class="hamburger-lines">
                <span class="line line1"></span>
                <span class="line line2"></span>
                <span class="line line3"></span>
            </div>
            <ul class="menu-items">
                <li><a href="#home">Home</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>
</template>

<style scoped>
.menu-items a {
    text-decoration: none;
    color: #444;
    font-weight: 500;
    transition: color 0.3s ease-in-out;
}

.menu-items a:hover {
    color: #117964;
    transition: color 0.3s ease-in-out;
}

.navbar {
    opacity: 0.95;
    position: fixed;
    width: 100%;
    color: #000;
    height: 50px;
    z-index: 12;
}

.navbar-container input[type="checkbox"],
.navbar-container .hamburger-lines {
    display: block;
}

.navbar-container {
    display: block;
    position: relative;
    height: 64px;
}

.navbar-container input[type="checkbox"] {
    position: absolute;
    display: block;
    height: 32px;
    width: 35px;
    top: 20px;
    right: 1rem;
    z-index: 5;
    opacity: 0;
}

.navbar-container .hamburger-lines {
    display: block;
    height: 23px;
    width: 35px;
    position: absolute;
    top: 17px;
    right: 1rem;
    z-index: 2;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.navbar-container .hamburger-lines .line {
    display: block;
    height: 4px;
    width: 100%;
    border-radius: 10px;
    background: #333;
}

.navbar-container .hamburger-lines .line1 {
    transform-origin: 0% 0%;
    transition: transform 0.4s ease-in-out;
}

.navbar-container .hamburger-lines .line2 {
    transition: transform 0.2s ease-in-out;
}

.navbar-container .hamburger-lines .line3 {
    transform-origin: 0% 100%;
    transition: transform 0.4s ease-in-out;
}

.navbar .menu-items {
    padding-top: 100px;
    background: #fff;
    height: 100vh;
    max-width: 400px;
    transform: translate(150%);
    display: flex;
    flex-direction: column;
    margin-left: 50px;
    padding-left: 50px;
    transition: transform 0.5s ease-in-out;
    box-shadow: 5px 0px 10px 0px #aaa;
}

.navbar .menu-items li {
    margin-bottom: 1.5rem;
    font-size: 1.3rem;
    font-weight: 500;
    list-style: none;
}


.navbar-container input[type="checkbox"]:checked~.menu-items {
    transform: translateX(0);
}

.navbar-container input[type="checkbox"]:checked~.hamburger-lines .line1 {
    transform: rotate(35deg);
}

.navbar-container input[type="checkbox"]:checked~.hamburger-lines .line2 {
    transform: scaleY(0);
}

.navbar-container input[type="checkbox"]:checked~.hamburger-lines .line3 {
    transform: rotate(-35deg);
}


@media screen and (min-width: 768px) {

    .navbar * {
        position: unset;
    }

    .navbar {
        height: 64px;
        background: none;
        padding: 0 2rem;
        max-width: 1280px;
    }

    .navbar-container input[type="checkbox"],
    .navbar-container .hamburger-lines {
        display: none;
    }

    .navbar-container {
        height: 64px;
        display: flex;
        justify-content: flex-end;
        
    }

    .navbar .menu-items {
        padding-top: 0;
        height: auto;
        transform: translate(0);
        box-shadow: none;
        background: none;
        display: flex;
        flex-direction: row;
        gap: 1.5rem;

        align-items: center;
        margin-right: 0px;
        margin: 0px;
        padding: 0px;

    }
}
</style>