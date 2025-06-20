<svelte:head>
  <link href="https://fonts.googleapis.com/css2?family=Inria+Sans&display=swap" rel="stylesheet" />
  <link href="https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap" rel="stylesheet" />
</svelte:head>

<script>
  let name = "";
  let phone = "";
  let location = "";
  let email = "";
  let password = "";

  function handleSubmit(e) {   /*to be done*/
    e.preventDefault();
    console.log({name, phone, location, email,password });
  }

  function handleLogin(e) {   /*to be done*/
    e.preventDefault();
    window.location.href = '/login';
  }
</script>

<style>
  /* background w gradient */
  .page-background {
    position: relative;
    width: 100vw;
    height: 100vh;
    overflow: hidden;
  }
  .page-background::before {
    content: "";
    position: absolute;
    inset: 0;
    background: linear-gradient(
      190.19deg,
      #01E8FA -7%,
      #01CFF7 0%,
      #01D6F4 0%,
      #039FF1 1%,
      #074F88 11%,
      #005698 20%,
      #001423 30%,
      #000910 35%
    );
    transform: matrix(-1, 0, 0, 1, 0, 0);
    z-index: -1;
  }

  /* for "Let's Get Started" */
  .heading {
    position: absolute;
    left: 4.0625rem;
    top: 9.6875rem;
    font-family: 'Inria Sans', sans-serif;
    font-weight: bold;
    font-size: 2.5rem;
    line-height: 3rem;
    color: white;
  }

  /* The rounded box */
  .registration-box {
    position: absolute;
    left: 50%;
    top: 9.6875rem;
    transform: translateX(-50%);
    width: 32.625rem;
    height: 40.0625rem;
    border: 0.0625rem solid #FFF9F9;
    border-radius: 7.25rem;
  }

  /* Form elements */
  .input-rect {
    position: absolute;
    background: #305168;
    border-radius: 0.625rem;
    color: white;
    padding-left: 0.9375rem;
    border: none;
    font-family: 'Inter', sans-serif;
    font-weight: 300;
    font-size: 1rem;
    line-height: 1.625;
  }
  label {
    position: absolute;
    color: white;
    font-family: 'Inter', sans-serif;
    font-weight: 700;
    font-size: 1rem;
    line-height: 1.1875rem;
  }
  input::placeholder {
    color: #D9D9D9;
    opacity: 1;
  }

  .name-label { left: 6.5rem; top: 3.875rem; width: 27.8125rem; height: 1.0625rem; }
  .name-input { left: 6.5rem; top: 5.5625rem; width: 19.734rem; height: 3.02625rem; }

  .phone-label { left: 6.5rem; top: 9.875rem; }
  .phone-input { left: 6.5rem; top: 11.5625rem; width: 19.734rem; height: 3.02625rem; }

  .location-label { left: 6.5rem; top: 15.875rem; }
  .location-input { left: 6.5rem; top: 17.5625rem; width: 19.734rem; height: 3.02625rem; }

  .email-label { left: 6.5rem; top: 21.875rem; }
  .email-input { left: 6.5rem; top: 23.5625rem; width: 19.734rem; height: 3.02625rem; }

  .password-label { left: 6.5rem; top: 27.875rem; }
  .password-input { left: 6.5rem; top: 29.5625rem; width: 19.734rem; height: 3.02625rem; }

  .login-link {
    position: absolute;
    left: 19.8125rem;
    top: 33.75rem;
    font-family: 'Inter', sans-serif;
    font-weight: 400;
    font-size: 0.9375rem;
    line-height: 1.125rem;
    color: white;
  }

  .register-button {
    position: absolute;
    left: 10.5rem;
    top: 35.25rem;
    width: 11.8125rem;
    height: 2.75rem;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 0.683125rem 2.188rem;
    gap: 0.68375rem;
    background: linear-gradient(99.74deg,#00121F 5.23%,#06BAF1 92.7%);
    border-radius: 3.418625rem;
    font-family: 'Inter', sans-serif;
    font-weight: 400;
    font-size: 1.230706rem;
    line-height: 1.6;
    color: white;
  }

</style>

<div class="relative overflow-hidden page-background">
  <h1 class="heading">Let's get started</h1>

  <div class="registration-box">
    <form on:submit={handleSubmit}>
      <label for="name" class="name-label">Name</label>
      <input id="name" class="name-input input-rect" type="text" bind:value={name} placeholder="Name" />

      <label for="phone" class="phone-label">Phone Number</label>
      <input id="phone" class="phone-input input-rect" type="text" bind:value={phone} placeholder="Phone Number" />

      <label for="location" class="location-label">Currently In</label>
      <input id="location" class="location-input input-rect" type="text" bind:value={location} placeholder="-- Currently In --" />

      <label for="email" class="email-label">Email</label>
      <input id="email" class="email-input input-rect" type="email" bind:value={email} placeholder="Email ID" />

      <label for="password" class="password-label">Password</label>
      <input id="password" class="password-input input-rect" type="password" bind:value={password} placeholder="Password" />

      <a href="/login" on:click={handleLogin} class="login-link">Login Instead</a>  

      <button type="submit" class="register-button">Register</button>
    </form>
  </div>

</div>
