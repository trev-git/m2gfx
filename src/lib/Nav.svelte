<script>
</script>

<nav class="navbar">
  <img src="M2Logo.svg" alt="logo">
  <ul class="menu-points">
    <li class="nav-item"><a href="/">Home</a></li>
    <li class="nav-item"><a href="/works">Works</a></li>
    <li class="nav-item"><a href="/contact">Contact</a></li>
    <li class="nav-item order"><a href="/order">Order</a></li>
  </ul>
</nav>

<style>
  .navbar {
    display: flex;
    flex-direction: row;
    padding: 1rem 3rem;
    justify-content: space-between;
    align-items: center;
  }
  .menu-points {
    display: flex;
    padding: 0;
    flex-direction: row;
  }
  .nav-item {
    color: white;
    list-style: none;
    font-family: 'Poppins';
    padding: 5px 20px;
    cursor: pointer;
  }
  .order {
    color: black;
    background-color: white;
    border-radius: 16px;
  }
  a {
    all: unset;
  }
</style>
