<script>
    export let educationData = {};
    const {Heading, Education_list} = educationData;
</script>

<style>
*,
*::before,
*::after {
  box-sizing: border-box;
}

/* html {
  background-color: #ecf9ff;
}

body {
  color: #272727;
  font-family: 'Quicksand', serif;
  font-style: normal;
  font-weight: 400;
  letter-spacing: 0;
  padding: 1rem;
} */

.main{
  max-width: 1200px;
  margin: 0 auto;
}

h1 {
    font-size: 24px;
    font-weight: 400;
    text-align: center;
}

img {
  height: auto;
  width: 50%;
  max-width: 100%;
  vertical-align: middle;
  /* justify-content: center */
  margin-left: 25%;
  padding-top: 3%;
  padding-bottom: 5%;
}

/* .btn {
  color: #ffffff;
  padding: 0.8rem;
  font-size: 14px;
  text-transform: uppercase;
  border-radius: 4px;
  font-weight: 400;
  display: block;
  width: 100%;
  cursor: pointer;
  border: 1px solid rgba(255, 255, 255, 0.2);
  background: transparent;
} */

/* .btn:hover {
  background-color: rgba(255, 255, 255, 0.12);
} */

.cards {
  display: flex;
  flex-wrap: wrap;
  list-style: none;
  margin: 0;
  padding: 0;
}

.cards_item {
  display: flex;
  padding: 1rem;
}

@media (min-width: 40rem) {
  .cards_item {
    width: 50%;
  }
}

@media (min-width: 56rem) {
  .cards_item {
    width: 33.3333%;
  }
}

.card {
  background-color: white;
  border-radius: 0.25rem;
  box-shadow: 0 20px 40px -14px rgba(0, 0, 0, 0.25);
  display: flex;
  flex-direction: column;
  overflow: hidden;
}

.card_content {
  padding: 1rem;
  background: linear-gradient(90deg, #9434ee 0%, #04caf1 100%);
  height: 100%
}

.card_title {
  color: #ffffff;
  font-size: 1.1rem;
  font-weight: 700;
  letter-spacing: 1px;
  text-transform: capitalize;
  margin: 0px;
  padding-bottom: 5%;
}

.card_text {
  color: #ffffff;
  font-size: 0.875rem;
  line-height: 1.5;
  margin-bottom: 1.25rem;    
  font-weight: 400;
}
</style>

<section id="education" class="section">
    <div class="main">
      <h1>{Heading}</h1>
  <ul class="cards section-body">
    {#each Education_list as list}
    <li class="cards_item">
      <div class="card">
        <div class="card_image"><img src={list.Image_url} alt={list.Label}></div>
        <div class="card_content">
          <h2 class="card_title">{list.Label}</h2>
          <p class="card_text">{list.Description}</p>
          <!-- <button class="btn card_btn">Read More</button> -->
        </div>
      </div>
    </li>
    {/each}
  </ul>
</div>
</section>