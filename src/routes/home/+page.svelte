<main>
  <header>
    <h1>Champions League</h1>
    <p>Följ alla matcher, nyheter och statistik från Europas största turnering</p>
  </header>



  <div class="container">
    <section class="section">
      <h2>Senaste Nyheter</h2>

    </section>

    <section class="section">
      <h2>Kommande Matcher</h2>
      <div class="match">
        <span>Inter</span>
        <span class="score">vs</span>
        <span>Manchester City</span>
      </div>
      <div class="match">
        <span>Liverpool</span>
        <span class="score">vs</span>
        <span>Real Madrid</span>
      </div>
      <div class="match">
        <span>PSG</span>
        <span class="score">vs</span>
        <span>Juventus</span>
      </div>
    </section>

    <section class="section">
      <h2>Senaste Resultat</h2>
      <div class="match">
        <span>Real Madrid</span>
        <span class="score">2 - 1</span>
        <span>Barcelona</span>
      </div>
      <div class="match">
        <span>Manchester Utd</span>
        <span class="score">1 - 3</span>
        <span>Liverpool</span>
      </div>
      <div class="match">
        <span>Bayern München</span>
        <span class="score">4 - 0</span>
        <span>Dortmund</span>
      </div>
    </section>

    <section class="section">
      <h2>Tabell</h2>
      <ul>
        <li>1. Manchester City - 12 poäng</li>
        <li>2. Real Madrid - 10 poäng</li>
        <li>3. PSG - 8 poäng</li>
        <li>4. Barcelona - 6 poäng</li>
        <li>5. Liverpool - 4 poäng</li>
      </ul>
    </section>
  </div>
</main>
<style>
  main {
    margin: 0;
    font-family: 'Segoe UI', sans-serif;
    background-color: #f5f7fa;
    color: #222;
  }

  header {
    background: linear-gradient(-45deg, #c609c6, #b92323);
    color: #fff;
    padding: 20px 0;
    text-align: center;
  }


  .container {
    max-width: 1000px;
    margin: 30px auto;
    padding: 0 20px;
  }

  .section {
    background-color: white;
    padding: 20px;
    border-radius: 8px;
    margin-bottom: 30px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
  }

  h2 {
    color: #003366;
    font-size: 22px;
    margin-bottom: 15px;
    border-bottom: 2px solid #0096c7;
    padding-bottom: 5px;
  }

  ul {
    list-style: none;
    padding: 0;
  }

  li {
    padding: 8px 0;
    border-bottom: 1px solid #eee;
  }

  .match {
    display: flex;
    justify-content: space-between;
    padding: 12px;
    border-radius: 6px;
    background-color: #f0f4f8;
    margin-bottom: 10px;
  }

  .score {
    font-weight: bold;
    color: #0096c7;
  }

</style>