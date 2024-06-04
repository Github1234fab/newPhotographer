<script>
        import { fade, slide } from "svelte/transition";
        import negrita from "../../Assets/Photos/NEGRITA.png";
        import rayban from "../../Assets/Photos/Rayban.jpg";
        import arbre from "../../Assets/Photos/Arbre de vie.png";
</script>

<main in:fade={{ duration: 2000 }}>
        <div class="wrapper-text">
                <h1>The Objects</h1>
                <p>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem explicabo perspiciatis minus
                        enim neque rem asperiores. Asperiores ea nobis exercitationem dignissimos. Quaerat quae fuga
                        modi iusto reiciendis saepe beatae vero?
                </p>
        </div>
        <div class="container">
                <div class="bloc-photo-fullPage"></div>
        </div>
        <div class="containerB">
                <div class="wrapper-3-photos">
                        <img src={negrita} alt="" class="img" />
                        <img src={rayban} alt="" class="img" />
                        <img src={arbre} alt="" class="img" />
                </div>
        </div>
</main>

<style>
        .container {
                display: flex;
                justify-content: center;
                align-items: center;
                height: 100vh;
                position: relative;
                margin-top: 100px;
        }
        .bloc-photo-fullPage {
                width: 100%;
                height: 500px;
                background-image: url("../../Assets/Photos/HeinekenII.jpg");
                background-repeat: no-repeat;
                background-size: contain;
                background-position: top;
        }
        .wrapper-text {
                position: absolute;
                top: 10%;
                left: 50%;
                transform: translate(-50%, 50%);
                gap: 20px;
                z-index: 1;
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
        }
        .img {
                width: auto;
                height: 340px;
                object-fit: contain;
                border-radius: 10px;
        }
        .wrapper-3-photos {
                height: 100vh;
                display: flex;
                justify-content: center;
                align-items: center;
                gap: 20px;
        }
        @media screen and (max-width: 768px) {
                .wrapper-text {
                        position: absolute;
                        top: 10%;
                        left: 50%;
                        transform: translate(-50%, 50%);
                        display: flex;
                        flex-direction: column;
                        justify-content: center;
                        align-items: center;
                        gap: 20px;
                }
                .bloc-photo-fullPage {
                        width: 100%;
                        height: 100%;
                        background-image: url("../../Assets/Photos/verres.jpg");
                        background-repeat: no-repeat;
                        background-size: 150%;
                        background-position: center left -250px;
                }
        }
</style>
