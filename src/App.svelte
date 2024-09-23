<script>
  import Background from './lib/Background.svelte';
  import pikrazimg from "./assets/images/pikrazimg.png";
  import tlg from './assets/icons/tlg.svg'
  import yt from './assets/icons/yt.svg'
  import x from './assets/icons/x.svg'

  let socials = $state([
    {
      name: "Twitter",
      link: "https://x.com/pikrazAirdrop",
      icon: x,
    },
    {
      name: `Youtube`,
      link: "https://www.youtube.com/@CriptoPikraz",
      icon: yt
    },
    {
      name: `Telegram`,
      link: "https://t.me/addlist/58relvZaYlFhOTFh",
      icon: tlg
    },
  ]);

 
</script>

<Background />
<main class="main">
  <article class="art">
    <section>
      <h1>Cripto Pikraz</h1>
      <figure>
        <img src={pikrazimg} width="120" height="120" alt="logo" class="img" />
      </figure>
    </section>

    <article class="socials">
      {#each socials as socialItem}
        <section class="cards">
          <a href={socialItem.link} target="_blank">
            <img src={socialItem.icon} alt={socialItem.name} width="30" height="30" />

            <span>
              
              {socialItem.name}
            </span>

          </a>
          <!-- <p>{socialItem.name}</p> -->
        </section>
      {/each}
    </article>
  </article>
</main>

<style>
  .main {
    display: grid;
    place-items: center;
    width: 100%;

    height: 100vh;

    text-align: center;

    & .art {
      background-color: #ffffff11;
      border-radius: 60px;
      border: 1px solid #fff;
      backdrop-filter: blur(2px);
      width: 80%;
      height: 90dvh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-between;
    }

    .img{
      filter: drop-shadow(-5px 5px rgba(72, 250, 226, 0.39));
    }
  }


  .socials{
    color: inherit;

display: grid;
grid-template-columns: repeat(1, 1fr);
grid-gap: 20px;
width: 90%;
margin-bottom: 30px;

    & .cards{
      padding: 10px;
border-radius: 20px;
      border: 1px solid #fff;
      background: #ffffff00;
    /* width: 100%; */
  
      display: flex;
      justify-content: space-around;
      background: rgba(72, 250, 226, 0.39);
      transition: .4s linear;

      & a{
        padding: 4px;
        display: flex;
        justify-content: start;
        align-items: center;
        

        text-decoration: none;
        
        width: 100%;
        color: inherit;

        & span{
          margin-left: 10px;
        }
        
      }

     
    }

    & .cards:hover{
      background: #7d6797a1;
    }
  }
</style>
