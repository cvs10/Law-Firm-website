<script>
  var prevScrollpos = window.pageYOffset;
  window.onscroll = function() {
    var currentScrollPos = window.pageYOffset;
    if (prevScrollpos > currentScrollPos) {
      document.getElementById("navbar").style.top = "0";
    } else {
      document.getElementById("navbar").style.top = "-50px";
    }
    prevScrollpos = currentScrollPos;
  };

    function uncheck(){
      document.getElementById("check").checked = false;
    }
  
</script>

<style>
  * {
    padding: 0;
    margin: 0;
    text-decoration: none;
    list-style: none;
    box-sizing: border-box;
  }

  nav {
    position: fixed;
    background: white;
    height: 3em;
    width: 100%;
    transition: top 0.4s;
    box-shadow: 5px 5px 5px -5px #000000;
    z-index: 10000;
  }

  a.logo {
    display: inline-block;
    color: black;
    font-size: 2rem;
    font-weight: bold;
    padding: 0 80px;
    opacity: 0.8;
    height: 50px;
  }

  a.logo p {
    position: relative;
    top: -42px;
    left: 40px;
    padding-left: 6px;
    font-family: "Open Sans", sans-serif;
    font-size: 0.8rem;
    font-weight: 700;
  }

  a.logo:hover {
    background: none;
  }

  .tel, .mail {
    display: inline-block;
    position: absolute;
    left: 300px;
    top: 2px;
    font-size: .8rem;
    text-transform: lowercase;
    font-weight: bold;

  }

  .tel {
    padding-left: -100px;
  }

  .mail {
    padding-left: 180px;
  }

  nav ul {
    display: flex;
    flex-direction: row;
    float: right;
    margin-right: 40px;
  }

  nav ul li {
    display: flex;
    margin: 0 5px;
  }

  nav ul li a {
    padding: 12px 16px;
    display: block;
    text-transform: uppercase;

    font-family: "Open Sans", sans-serif;
    color: black;
    opacity: 0.9;
  }

  a.link:hover {
    background: rgba(176, 219, 245, 0.452);
    transition: 0.2s;
    border-bottom: 3px solid black;
  }

  label {
    position: relative;
    display: block;
    float: right;
  }

  .checkbtn {
    font-size: 2rem;
    margin-right: 16px;
    cursor: pointer;
    display: none;
  }

  #check {
    display: none;
  }

  .additionalPhone,
  .contactForm {
    display: none;
  }

  @media (max-width: 858px) {
    .checkbtn {
      display: block;
    }

    a.logo {
      padding-left: 20px;
    }

    nav ul {
      position: fixed;
      display: flex;
      flex-direction: column;
      width: 100%;
      height: 100vh;
      background: white;
      top: 48px;
      left: -100%;
      text-align: center;
      transition: all 0.5s;
    }
    nav ul li:first-child {
      margin-top: 40px;
    }

    nav ul li {
      display: flex;
      flex-direction: column;
      margin-top: 10px;
       
      margin-left: 5%;
      margin-right: 5%;
      margin-top: 2%;
    }

    nav ul li a {
      font-weight: bold;
      border: 1px solid black;
    }

    #check:checked ~ ul {
      left: 0;
    }

    .tel, .mail {
      display: none;
    }

    .additionalPhone, 
    .contactForm {
    display: block;
    
  }
  .additionalPhone {
    color:#df2020;
  }
  }
</style>

<nav id="navbar">
  <input type="checkbox" id="check" />
  <label for="check" class="checkbtn">
    <i class="fas fa-bars" />
  </label>
  <a href="#title" class="logo" on:click={uncheck}>
    <i class="fas fa-balance-scale" />
    <p>Kancelaria Adwokacka</p>
    <p>Mariusz Misiorek</p>
  </a>
  <ul id="menu">
    <li>
      <a class="tel" href="tel:+48602336862">Tel. +48 602 336 862</a>
    </li>
    <li>
      <a class="mail" href="mailto:kancelaria@adwokatmisiorek.pl">E-mail: kancelaria@adwokatmisiorek.pl</a>
    </li>
    <li>
      <a class="link" href="#kancelaria" on:click={uncheck}>Kancelaria</a>
    </li>
    <li>
      <a class="link" href="#specjalizacje" on:click={uncheck}>Specjalizacje</a>
    </li>
    <!-- <li>
      <a class="link" href="#opinie" on:click={uncheck}>Opinie</a>
    </li> -->
    <li>
      <a class="link" href="#kontakt" on:click={uncheck}>Kontakt</a>
    </li>
    <li>
      <a class="link contactForm" href="#formularz" on:click={uncheck}>Formularz kontaktowy</a>
    </li>
    <li>
      <a class="link additionalPhone" href="tel:+48602336862" on:click={uncheck}>Tel. +48 602 336 862</a>
    </li>
  </ul>
</nav>
