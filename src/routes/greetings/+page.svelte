<script>
  let username="username";
  let caCode = '';
  const enterCode = () => {
    alert(`Entered CA code: ${caCode}`);
  };
  const getCode = () => {
    alert('Generating CA code...');
  };
</script>
<style>
  :global(body){
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  .container {
    padding: 0;
    height: 100%;
    width: 100%;
    background-image: none;
    background-color: #444;
    background: linear-gradient(
  190deg,
  #01d6f4 0%,
  #039ff1 1%,
  #0575ba 1%,
  #074f88 1%,
  #04528e 1%,
  #005698 2%,
  #001423 26%,
  #000910 30%,
  #000000 40%,
  #000000 100%
);


    color: white;
    min-height: 100vh;
    font-family: 'Segoe UI', sans-serif;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding: 2rem;
  }

  .header {
    font-size: 1.2rem;
    text-transform: uppercase;
    letter-spacing: 1px;
    color: #ccc;
  }

  .main {
    flex: 1;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
  }

  .left {
    max-width: 50%;
  }

  h1 {
    font-size: 3rem;
    margin-bottom: 1rem;
  }

  h1 span {
    color: #3fdcff;
  }

  p {
    margin-bottom: 2rem;
    font-size: 1.1rem;
    color: #ccc;
  }

  .buttons button {
    font-family: Arial, Helvetica, sans-serif;
    margin: 1rem;
    padding: 0.8rem 1.5rem;
    border: none;
    border-radius: 25px;
    font-size: 1rem;
    cursor: pointer;
    background: linear-gradient(120deg, #000000, #01CFF7);
    color: white;
    transition: transform 0.2s ease;
    display: flex;
    justify-content: flex-start;
  }

  .buttons button:hover {
    transition: transform 0.2s ease;
    transform: scale(1.05);
    
  }

  .hands {
    max-width: 40%;
    height: max-content;
  }

  .footer {
    height: 40px;
    display:inline-flex;
    justify-content: space-around;
    padding: 1rem;
    border-top: 1px solid #444;
    font-size: 0.9rem;
    color: #aaa;
  }

  .footer span {
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }
  .globe{
    height: 40px;
    display: inline-flex;
  }
  @media(max-width:768px){
    .hands{
      display: none;
    }
  }
</style>

<div class="container">
  <span class="header">PETRICHOR' 26</span>

  <div class="main">
    <div class="left">
      <h1>Hi, <span>{username}</span></h1>
      <p>I was struggling while adding gradient  =(
      </p>
      <div class="buttons">
        <button on:click={enterCode}>Enter CA code</button>
        <button on:click={getCode}>Get CA code</button>
      </div>
    </div>

    <div class="hands">
      <img src="src/lib/hands.png" alt="HandsIMG" style="width: 100%;" />
    </div>
  </div>

  <div class="footer">
    <div class="globe">
      <img src="src/lib/globe.png" alt="GlobeIMG">
      <span>PETRICHOR</span>
    </div>
    <div class="globe">
      <img src="src/lib/globe.png" alt="GlobeIMG">
      <span>PETRICHOR</span>
    </div>
    <div class="globe">
      <img src="src/lib/globe.png" alt="GlobeIMG">
      <span>PETRICHOR</span>
    </div>
    
  </div>
</div>