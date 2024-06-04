<script>
        let subMenuRef;
        let headerRef;

        import { onMount } from "svelte";

        onMount(() => {
                window.addEventListener("click", () => {
                        subMenuRef.style.display = "none";
                });
        });

        //      ..................................................................................................................................................

        function headerBgColor() {
                headerRef.style.backgroundColor = "rgba(0, 0, 0, 0.2)";
                headerRef.style.transition = "0.6s ease-in-out";
                console.log(3);
        }

        function headerBgColorRemove() {
                headerRef.style.backgroundColor = "transparent";
                headerRef.style.transition = "0.6s ease-in-out";
        }

        function subMenuDisplayNone() {
                setTimeout(() => {
                        subMenuRef.style.display = "none";
                }, 1200);
        }

        //     ................................................................................................................

        //fonctions pour activer et desactiver les couleurs du header
        function displayMenu() {
                subMenuRef.style.display = "block";
        }
</script>

<header bind:this={headerRef}>
        <a href="/" class="logo">Home</a>

        <nav>
                <a href="/Portfolio" class="link" on:mouseenter={displayMenu} on:mouseover={headerBgColor} on:focus={headerBgColor} on:blur={headerBgColorRemove} on:mouseout={headerBgColorRemove}>Portfolio </a>
                <a href="/Profil" class="link" on:mouseover={headerBgColor} on:focus={headerBgColor}>Profil</a>
                <a href="/Contact" class="link" on:mouseover={headerBgColor} on:focus={headerBgColor}>Contact</a>

                <div class="subMenu" role="menu" tabindex="0" bind:this={subMenuRef} on:mouseleave={subMenuDisplayNone}>
                        <ul class="subMenu-list">
                                <a href="/Portraits" class="link-subMenu">Portraits</a>
                                <a href="/Objets" class="link-subMenu">Objets</a>
                                <a href="/Paysages" class="link-subMenu">Paysages</a>
                                <a href="/Abstraits" class="link-subMenu">Abstraits</a>
                        </ul>
                </div>
        </nav>
</header>

<style>
        header {
                display: flex;
                justify-content: space-between;
                align-items: center;
                padding: 2rem;
                color: white;
                z-index: 999;
                transition: 0.6s ease-in-out;
        }

        nav {
                display: flex;
                gap: 30px;
                position: relative;
        }
        .link {
                text-decoration: none;
                color: black;
                font-size: 1.3rem;
                transition: 0.6s ease-in-out;
                min-width: 90px;
                text-align: center;
                transition: 0.6s ease-in-out;
                font-weight: 500;
        }
        .subMenu {
                position: absolute;
                top: 70px;
                left: -33px;
                right: 0;
                bottom: 0;
                display: none;
                animation: scale 0.8s ease-in-out;
                background-color: rgb(255, 255, 255);
                backdrop-filter: blur(20px);
                z-index: 999;
        }

        .subMenu-list {
                display: flex;
                flex-direction: column;
                gap: 20px;
                justify-content: center;
                align-items: center;
                color: black;
                padding: 40px 20px;
                border-radius: 10px;
                box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
                max-width: 150px;
                box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.355);
                font-weight: 500;
                transition: 0.7s ease-in-out;
        }
        .link-subMenu {
                text-decoration: none;
                color: black;
                font-size: 1.1rem;
        }
        .link-subMenu:hover {
                color: blue;
        }
        .link:hover {
                color: white;
        }
        .logo {
                text-decoration: none;
                color: black;
                font-size: 1.3rem;
        }
        .logo:hover {
                color: white;
        }

        @keyframes scale {
                0% {
                        transform: scale(0.3);
                }
                100% {
                        transform: scale(1);
                }
        }
</style>
