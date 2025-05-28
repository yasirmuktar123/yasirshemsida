<main>
  <div class="container">
    <h1>Registrering</h1>
    <form>
      <label for="name">Namn:</label>
      <input type="text" id="name" />

      <label for="email">E-post:</label>
      <input type="email" id="email" />

      <label for="password">Lösenord:</label>
      <input type="password" id="password" />

      <label for="color">Favoritfärg:</label>
      <select id="color">
        <option value="röd">Röd</option>
        <option value="blå">Blå</option>
        <option value="grön">Grön</option>
        <option value="gul">Gul</option>
      </select>

      <input type="submit" value="Registrera" />
    </form>
  </div>
</main>

<style>
  main {
    background: linear-gradient(-45deg, #c609c6, #b92323);
    width: 100%;
    height: 100vh;
    padding: 5%;
  }

  .container {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
    border: solid 5px #b20606;
    border-radius: 10px;
    width: 25%;
    min-width: 300px;
    background-color: #3a2e3b;
    margin: auto;
    padding: 25px;
    color: #b20606;
    box-shadow: 0 0 15px rgba(178, 6, 6, 0.3);
  }

  form {
    display: flex;
    flex-direction: column;
    gap: 15px;
    width: 100%;
  }

  label {
    font-weight: bold;
    color: rosybrown;
  }

  input, select {
    padding: 8px;
    border-radius: 5px;
    border: 2px solid #b20606;
    background-color: #4a3a4b;
    color: rosybrown;
  }

  input[type="submit"] {
    background-color: #b20606;
    color: white;
    font-weight: bold;
    padding: 10px;
    cursor: pointer;
    transition: all 0.3s ease;
    border: none;
  }

  input[type="submit"]:hover {
    background-color: #8a0505;
    transform: scale(1.02);
  }

  h1 {
    color: rosybrown;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
  }
</style>