<script>
import CardService from './CardService.vue'
import ReservationBtn from '../ReservationBtn.vue'


export default {
    data() {
        return {};
    },
    components: {
        CardService,
        ReservationBtn

    },
}
</script>
<template>
    <footer>
        <div class="footer-title">
            <h1>Alors intéresser <span>?</span></h1>
        </div>
        <div class="footer-content">
            <div class="footer-content-title">
                <h2>Nous somme là !</h2>
            </div>
            <div class="google-map-academie-gold">
                <!-- <img src="../../assets/google-academie-gold.png" alt="" srcset=""> -->
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2791.0739773855316!2d-73.51813582505909!3d45.609157323757096!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x4cc905909f7ec281%3A0xb7cc7e56f6daa4ac!2sAcad%C3%A9mie%20Gold%20Studio!5e0!3m2!1sfr!2sca!4v1711307610609!5m2!1sfr!2sca" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
            </div>
            <div class="footer-info-container">
                <div class="footer-general-info">
                    <p class="title-footer-general-info">Adresse :</p>
                    <p>9468 rue Hochelaga, Montréal,QC</p>
                    <p class="title-footer-general-info">Téléphone :</p>
                    <p>(---) --- ----</p>
                    <p class="title-footer-general-info">Courriel :</p>
                    <p>academiegold@info.com</p>
                    <p class="title-footer-general-info">Horaire du salon :</p>
                    <p>10h00 À 19h00</p>
                </div>
                <div class="footer-reservation">
                    <h2>Réserver avec nous</h2>
                    <ReservationBtn></ReservationBtn>

                </div>
                <div class="footer-social">
                    <a href="https://www.instagram.com/academiegoldstudio/"> <img
                            src="../../assets/icon-instagram-academie-gold.png" alt="">
                    </a>
                    <a href="https://www.facebook.com/profile.php?id=100075989584620"> <img src="../../assets/icon-facebook-academie-gold.png" alt="">
                    </a>

                </div>

            </div>
            <div class="credit">
                <p>Fait avec amour et passion par <a href="https://jappfiction.com/">Jappfiction</a></p>
                <p>Photos fait par <a href="https://www.instagram.com/mxrcx.225/">𝐌𝐚𝐫𝐜-𝐀𝐧𝐭𝐨𝐢𝐧𝐞</a></p>

            </div>


        </div>



    </footer>

</template>
<style scoped>
footer {
    width: 100vw;
}

span {
    color: #CFA246;
}

.footer-title {
    height: 20vh;
    width: 100vw;
    color: white;
    margin-bottom: 20vh;
}

.footer-title>h1 {
    font-size: 5em;
    color: white;

}

.footer-content {
    width: 100vw;
    display: flex;
    flex-direction: column;
    justify-content: center;
    background-color: #464545;


}

.footer-content-title {
    margin-left: 5vw;
    font-size: 2em;
}

.google-map-academie-gold {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.google-map-academie-gold>img {
    width: 90%;

}
iframe{
    height: 80vh;
    width: 90%;
}

.footer-info-container {
    width: 90%;
    margin-left: 5vw;
    display: flex;

    justify-content: space-between;

}

.title-footer-general-info {
    color: white;

    font-weight: bold;
    font-size: 1.2em;
}

.footer-reservation {
    display: flex;
    align-items: center;
    flex-direction: column
}

.footer-social {
    width: 10%;
    height: 40vh;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: flex-end;
}

.credit {
    width: 90%;
    margin-left: 5vw;
    display: flex;

    justify-content: space-between;
    align-items: center;
}

.credit>p>a {
    color: red
}
</style>