
<div class="container">
        <div class="hero">
                <div class="wrapper-heroText-list">
                        <h1 class="hero-text">Welcome to my Portfolio</h1>
                        <ul class="liste">
                                <a href="/Portraits" class="style-link">Portraits</a>
                                <a href="/Objets" class="style-link">Objets</a>
                                <a href="/Paysages" class="style-link">Paysages</a>
                                <a href="/Abstrait" class="style-link">Abstrait</a>
                        </ul>
                </div>
        </div>
</div>

<style>
        .hero {
                height: 100vh;
                margin-top: -100px;
                background-image: url("../Assets/NYCABlack.png");
                background-size: cover;
                background-position: center;
                background-repeat: no-repeat;
                z-index: 0;
                margin-bottom: -100px;
        }
        .wrapper-heroText-list {
                position: absolute;
                top: -340px;
                left: 50%;
                transform: translate(-50%, 50%);
                z-index: 1;
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
        }
        .hero-text {
                color: black;
                font-size: 3rem;
                text-align: center;
                margin-top: 300px;
        }
        .liste {
                display: flex;
                gap: 20px;
                z-index: 0;
        }
        .style-link {
                text-decoration: none;
                color: black;
                font-size: 1.3rem;
        }

        @media screen and (max-width: 768px) {
                .wrapper-heroText-list {
                        top: -400px;
                        left: 50%;
                        transform: translate(-50%, 50%);
                        align-items: center;
                        justify-content: center;
           
                }
        }
        @media screen and (max-width: 578px) {
                .wrapper-heroText-list {
                        top: -400px;
                        left: 50%;
                        transform: translate(-50%, 50%);
                     align-items: center;
                        justify-content: center;
                }
        }
</style>
