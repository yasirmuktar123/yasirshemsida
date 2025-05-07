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
      background-repeat: repeat;
      width: 100%;
      height: 100%;
      padding: 5%;
      background: linear-gradient(-45deg, #c609c6, #b92323);
    }
  
    .container {
      display: flex;
      flex-direction: column;
      justify-content: space-evenly;
      align-items: center;
      border: solid 5px rosybrown;
      border-radius: 10px;
      width: 25%;
      height: 50%;
      background-color: #3a2e3b;
      margin: auto;
      padding: 20px;
      color: rgb(186, 7, 7);
    }
  
    form {
      display: flex;
      flex-direction: column;
      gap: 10px;
      width: 100%;
    }
  
    label {
      font-weight: bold;
    }
  
    input, select {
      padding: 5px;
      border-radius: 5px;
      border: none;
    }
  
    input[type="submit"] {
      background-color: rgb(55, 53, 53);
      color: rgb(186, 139, 139);
      font-weight: bold;
      cursor: pointer;
      transition: background-color 0.3s;
    }
  
    input[type="submit"]:hover {
      background-color: #b32222;
    }
  </style>
  