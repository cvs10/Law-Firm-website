<script>
let firstName = "";
let lastName = "";
let email = "";
let tel = "";
let message = "";


    function popUp(){
        document.getElementById("rodo").style.visibility = "visible";
    }


    function sendEmail(){
            Email.send({
    SecureToken : "1a85a797-39f3-414d-87ad-0af8a67e5151",
    To : 'kancelaria.formularz@gmail.com',
    From : "kancelaria.formularz@gmail.com",
    Subject : "Formularz kontaktowy",
    Body : `imię: ${firstName}<br>
            nazwisko: ${lastName}<br>
            email: ${email}<br>
            telefon: ${tel}<br><br>
            wysłał wiadomość: ${message}`,
    
    
    // "imię: "+ firstName +"nazwisko: "+lastName+"email: "+ email +"telefon: "+ tel + "wiadomość: "+ message, 
}).then(
  message => alert("Wiadomość została poprawnie wysłana.")
);
    document.getElementById("rodo").style.visibility = "hidden";
    firstName = "";
    lastName = "";
    email = "";
    tel = "";
    message = "";
}

function brakZgody(){
    alert("Formularz nie został wysłany");
    document.getElementById("rodo").style.visibility = "hidden";
}



</script>

<style>
    main {
        background-color: #F4F5F5;
        position: absolute;
        height: auto;
        width: 100vw;
        padding: 100px 20%;
    }
    

    #adress {
        height: auto;
        width: 100%;
        margin-bottom: 10px;
        border-radius: 10px;
        background-color: rgba(255, 255, 255, 0.705);
    }

    .contact-form-withMap {
        display: flex;
        flex-direction: row;
        height: 600px;
        width: 100%;
    }

    #map {
        position: relative;
        width: 50%;
        height: 100%;
        margin-right: 5%;
        border-radius: 10px;
        background-color: white; 
    }

    #formularz {
        position: relative;
        width: 50%;
        height: 100%;
        border-radius: 10px;
        background-color: white;
    }

    iframe {
        display:block;
        width: 100%;
        height: 85%;
        border-radius: 10px;
    }

    .mapLinksDiv{
        display: flex;
        flex-direction: row;
        
        
    }

    .mapLinks {
        width: 49%;
        height: 50px;
        margin-left: .5%;
        border: 1px solid black;
        text-align: center;
        text-decoration: none;
        border-radius: 5px;
        background-color: white;
    }

    .mapLinks a {
        display: block;
        color: black;
        transform: translateY(50%);
        text-decoration: none;
    }
    

    .bi {
        font-size: 2rem;
        color: rgb(3, 108, 245);
        padding-right: 1.5rem;
        padding-left: .5rem;
    }

    p {
        display: inline-block;
        font-size: 1.5rem;
        color: black;
    }

    #adress a{
        font-size: 1.5rem;
        color: black;
        text-decoration: none;
    }

    /* Contact form */
    /* ---------------------------- */

    #formularz p {
        padding-top: 5px;
        padding-left: 15px;
    }
    .form-group {
        width: 100%;
        margin-top: -5px;
        font-size: .9rem;
        margin-left: 15px;
        margin-right: 15px;
    }

    .form-group input,
    .form-group textarea {
        width: 94%;
        padding: 2px;
        font-size: .9rem;
    }

    textarea {
        resize: vertical;
    }

    input[type="button"] {
        width: 94%;
        height: 50px;
        margin-left: 15px;
        border-radius: 5px;
        transition: .3s ease background-color;
    }

    input[type="button"]:hover {
        background-color: aliceblue;
    }


    /* ------------------------------ */


    @media (max-width: 1368px) {
        main {
        background-color: #F4F5F5;
        position: absolute;
        height: auto;
        width: 100vw;
        padding: 100px 10%;
    }
    }

    @media (max-width: 858px) {
        main {
        background-color: #F4F5F5;
        position: absolute;
        height: auto;
        width: 100vw;
        padding: 60px 5px;
    }


        .contact-form-withMap {
        display: flex;
        flex-direction: column;
        height: 900px;
        width: 100%;
        margin-top: 30px;
        
    }

    #map {
        position: relative;
        width: 100%;
        height: 300px;
        margin-right: 0%;
        border-radius: 10px;
        background-color: white;
        margin-bottom: 70px;
        
    }

    #formularz {
        position: relative;
        width: 98%;
        height: 600px;
        margin-top: 20px;
        border-radius: 10px;
        background-color: white;
    }

    #adress a{
        font-size: 1rem;
        color: black;
        text-decoration: none;
        padding-left: 10px;
    }

    .bi {
        font-size: 1.2rem;
        padding-right: .2rem;
        padding-left: .5rem;
    }
    .newLine {
        padding-left: 40px;
    }
    }
/* RODO window -------------------------*/
#rodo {
    visibility: hidden;
    position: absolute;
    left: 0;
    top: 0;
    transform: translate(70%, 50%);
    height: 350px;
    width: 40%;
    background-color: black;
    color: white;
    border-radius: 2%;
}

#rodo h4 {
    padding: 20px;
    text-align: justify;
    font-family: "Open Sans", sans-serif;
    font-size: 1.2rem;
}

.rodo-btn {
    width: 40%;
    margin-left: 7%;
    margin-top: 20px;
}


@media (max-width: 1368px) {
#rodo {
    position: absolute;
    left: 0;
    top: 22%;
    transform: translate(50%, 50%);
    height: 350px;
    width: 50%;
    background-color: black;
    color: white;
    border-radius: 2%;
    
}

#rodo h4 {
    padding: 20px;
    text-align: justify;
    font-family: "Open Sans", sans-serif;
    font-size: 1.2rem;
}

.rodo-btn {
    width: 40%;
    margin-left: 7%;
}
}
@media (max-width: 858px) {

    #rodo {
    top: 50%;
    transform: translate(5%, 5%);
    height: 350px;
    width: 92%;
    border-radius: 2%;
    
}

#rodo h4 {
    padding: 20px;
    text-align: justify;
    font-family: "Open Sans", sans-serif;
    font-size: .8rem;
}

.rodo-btn {
    width: 40%;
    margin-left: 7%;
    font-size: .7rem;
}
}

    
</style>

<main id="kontakt">
    <h3>Kontakt</h3>
    <div id="adress">
        <i class="bi bi-geo-alt"></i>
        <a href="https://www.google.com/maps/place/Zieleniak,+Kupiecka,+80-001+Gda%C5%84sk,+Polska/@54.3582645,18.6449018,17z/data=!4m5!3m4!1s0x46fd73712844bd79:0x1608369a51ded944!8m2!3d54.3584271!4d18.6464253" target="_blank">Ul. Wały Piastowskie 1 lok. 1203C <spam class="newLine">("Zieleniak" piętro 12)</spam></a>
        <br>
        <i class="bi bi-telephone"></i>
        <a class="tel" href="tel:+48602336862">+48 602 336 862</a>
        <br>
        <i class="bi bi-envelope"></i>
        <a class="mail" href="mailto:kancelaria@adwokatmisiorek.pl">kancelaria@adwokatmisiorek.pl</a>
    </div>
    <div class="contact-form-withMap">
        <div id="map">
            <iframe title="map" frameborder="0" scrolling="no"  src="https://www.openstreetmap.org/export/embed.html?bbox=18.64238262176514%2C54.35655626208956%2C18.650536537170414%2C54.36037612657571&amp;layer=mapnik&amp;marker=54.35846623872907%2C18.646459579467773" style="border: 1px solid black"></iframe>
            <br/>
            <div class="mapLinksDiv">
                <div class="mapLinks biggerMap"><a href="https://www.openstreetmap.org/?mlat=54.35847&amp;mlon=18.64646#map=17/54.35847/18.64646" target="_blank">Powiększ mapę</a></div>
                <div class="mapLinks"><a href="https://www.google.com/maps/place/Zieleniak,+Kupiecka,+80-001+Gda%C5%84sk,+Polska/@54.3582645,18.6449018,17z/data=!4m5!3m4!1s0x46fd73712844bd79:0x1608369a51ded944!8m2!3d54.3584271!4d18.6464253" target="_blank">Szczegóły dojazdu</a></div>
            </div>
        </div>
        <div id=formularz>
            <p>Formularz kontaktowy</p>
            <form method="post" class="contact-form">
                <div class="form-group">
                    <label for="firstName">Imię</label>
                    <input type="text" id="firstName" name="firstName" bind:value={firstName}>
                </div>
                <div class="form-group">
                    <label for="lastName">Nazwisko</label>
                    <input type="text" id="lastName" name="lastName" bind:value={lastName}>
                </div>
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" name="email" bind:value={email}>
                </div>
                <div class="form-group">
                    <label for="tel">Telefon</label>
                    <input type="tel" id="tel" name="tel" bind:value={tel}>
                </div>
                <div class="form-group">
                    <label for="message">Wiadomość</label>
                    <textarea name="message" id="message" cols="30" rows="5" bind:value={message}></textarea>
                </div>
                <input type="button" value="Wyślij wiadomość" on:click="{popUp}"> 
            </form>
        </div>
        <div id="rodo">
            <h4>"Wypełnienie formularza oznacza, że podane w nim dane osobowe będą przetwarzane w celu kontaktu zwrotnego, ustosunkowania się do przedstawionego tematu lub propozycji konsultacji. Dane osobowe przetwarzane będą stosownie do zasad wynikających z treści rozporządzenia  Parlamentu  Europejskiego  i  Rady  (UE)  2016/679  z  dnia 27 kwietnia 2016 r. w sprawie ochrony osób fizycznych w związku z przetwarzaniem danych osobowych i  w  sprawie  swobodnego  przepływu  takich  danych  oraz  uchylenia  dyrektywy  95/46/WE  (ogólne rozporządzenie o ochronie danych) (Dz. Urz. UE L 119 z 04.05.2016)."</h4>
            <button class="rodo-btn" type="button" on:click="{sendEmail}">Wyrażam zgodę</button>
            <button class="rodo-btn" type="button" on:click="{brakZgody}">Nie wyrażam zgody</button>
        </div>
    </div>
</main>