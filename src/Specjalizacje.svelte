<style>
    main {
        height: 100vh;
        width: 100vw;
    }

    p {
        display: block;
        padding-top: 130px;
        padding-right: 20%;
        padding-left: 20%;
        text-align: justify;
        font-family: "Old Standard TT", serif;
        font-size: 1.2rem;
        font-weight: 500;
        color: black;
        line-height: 2;   
    }
    p:last-child {
        padding-top: 50px;
    }

    /* Specializacje */
    /* -------------------- */
    .spec-div {
        display: flex;
        flex-wrap: wrap;
        width: 60%;
        min-height: 400px;
        max-height: 100%;
        margin-top: 20px;
        margin-right: 20%;
        margin-left: 20%;
    }

    .spec-box {
        flex: 20%;
        margin-left: 1%;
        margin-right: 1%;
        margin-top: 1%;
        margin-bottom: 1%;
        width: 170px;
        height: 200px;
        border: .5px solid black;
        border-radius: 3px;
        background: rgba(176, 219, 245, 0.452);
        box-shadow: 5px 5px 7px -2px #000000;
    }

    .spec-box:hover {
        transform: scale(1.05);
        transition: .2s all;
    }

    .icon-box {
        height: 70%;
        width: 100%;
        border-bottom: .5px solid black;
        text-align: center;
    }

    .fas {
        position: relative;
        font-size: 6rem;
        transform: translateY(25%);
    }

    .text-box {
        height: 30%;
        width: 100%;
        text-align: center;
    }

    .text-box h3 {
        font-size: 1.5rem;
        font-family: "Old Standard TT", serif;
        transform: translateY(50%);
    }





    /* -------------------- */



    @media (max-width: 1368px) {
        p {
            padding: 60px 10% 0px 10%;
            font-size: 1.1rem;
            line-height: 1.6;
        }
        .text-box h3 {
        font-size: 1.1rem; 
        transform: translateY(90%);
        }

    }

    @media (max-width: 1024px) {

        main {
            height: auto;
        }

        p {
            padding: 80px 15px;
            font-size: 1.1rem;
            line-height: 1.8;
        
        }
        
    }

    @media (max-width: 858px) {
        main {
        padding-top: 20px;
        }

        .spec-div {
        display: flex;
        flex-wrap: wrap;
        width: 99%;
        min-height: 300px;
        max-height: 100%;
        margin-top: -70px;
        margin-right: .5%;
        margin-left: .5%;
    }

    .spec-box {
        flex: 40%;
        margin-left: 2%;
        margin-right: 2%;
        margin-top: 2%;
        margin-bottom: 2%;
        width: 100px;
        height: 140px;
        
    }

    .icon-box {
        height: 70%;
        width: 100%;
        border-bottom: .5px solid black;
        text-align: center;
    }

    .fas {
        position: relative;
        font-size: 4rem;
        transform: translateY(25%);
    }

    .text-box {
        height: 30%;
        width: 100%;
        text-align: center;
    }

    .text-box h3 {
        font-size: .9rem;
        font-family: "Old Standard TT", serif;
        transform: translateY(80%);
    }
    
    }

</style>

<main id="specjalizacje">
    <p>
        Zakres świadczonych usług obejmuje pomoc prawną dla klientów prywatnych – zarówno na etapie przedsądowym, jak i procesowym, a także kompleksową, bieżącą obsługę prawną przedsiębiorców.
        <br><br>Zasadnicze specjalizacje w mojej zawodowej praktyce to:
    </p>
    <div class="spec-div">
        <div class="spec-box">
            <div class="icon-box">
                <i class="fas fa-gavel"></i>
            </div>
            <div class="text-box">
                <h3>Prawo Karne</h3>
            </div>
        </div>
        <div class="spec-box">
            <div class="icon-box">
                <i class="fas fa-handshake"></i>
            </div>
            <div class="text-box">
                <h3>Prawo Cywilne</h3>
            </div>
        </div>
        <div class="spec-box">
            <div class="icon-box">
                <i class="fas fa-hand-holding-usd"></i>
            </div>
            <div class="text-box">
                <h3>Prawo Spadkowe</h3>
            </div>
        </div>
        <div class="spec-box">
            <div class="icon-box">
                <i class="fas fa-users"></i>
            </div>
            <div class="text-box">
                <h3>Prawo Rodzinne</h3>
            </div>
        </div>
        <div class="spec-box">
            <div class="icon-box">
                <i class="fas fa-donate"></i>
            </div>
            <div class="text-box">
                <h3>Prawo Bankowe</h3>
            </div>
        </div>
        <div class="spec-box">
            <div class="icon-box">
                <i class="fas fa-industry"></i>
            </div>
            <div class="text-box">
                <h3>Prawo Gospodarcze</h3>
            </div>
        </div>
        <div class="spec-box">
            <div class="icon-box">
                <i class="fas fa-id-card"></i>
            </div>
            <div class="text-box">
                <h3>Prawo Pracy</h3>
            </div>
        </div>
        <div class="spec-box">
            <div class="icon-box">
                <i class="fas fa-landmark"></i>
            </div>
            <div class="text-box">
                <h3>Prawo Administracyjne</h3>
            </div>
        </div>
    </div>
    <p>
        Realizowałem i realizuję również obsługę prawną obejmującą inne zakresy prawa, a każdy klient traktowany jest indywidualnie – w zależności od specyfiki jego sprawy oraz rzeczywistych potrzeb.
    </p>

</main>