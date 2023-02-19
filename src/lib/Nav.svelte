<script>
</script>

<nav class="navbar">
  <img class="nav-logo" src="M2Logo.svg" alt="logo">
  <ul class="menu-points">
    <li class="nav-item"><a href="/">home</a></li>
    <li class="nav-item"><a href="/works">works</a></li>
    <li class="nav-item"><a href="/contact">contact</a></li>
    <li class="nav-item order"><a href="/order">order</a></li>
  </ul>
</nav>

<style>
  .nav-logo {
    width: 80px;
  }
  .navbar {
    display: flex;
    position: sticky;
    top: 0;
    padding: 2rem 6rem;
    justify-content: space-between;
    align-items: center;
    background: linear-gradient(180deg, rgba(0,0,0,1) 0%, rgba(0,0,0,0) 100%);
    z-index: 1000;
  }
  .menu-points {
    display: flex;
    padding: 0;
    gap: 2rem;
  }
  .nav-item {
    transition: .2s;
    color: var(--secondary);
    list-style: none;
    font-family: 'Poppins';
    padding: 0.5rem 2rem;
    font-size: 1rem;
    font-weight: 800;
    line-height: 1.5rem;
    cursor: pointer;
  }
  .nav-item:hover:not(:last-child) {
    transition: .2s;
    color: var(--accent-two);
    padding-inline: 3rem;
    outline: solid 1px var(--accent-two);
    border-radius: 1000px;
  }
  .order {
    transition: .2s;
    color: var(--secondary-two);
    background-color: var(--secondary);
    border-radius: 10rem;
  }
  .order:hover {
    transition: .2s;
    padding-inline: 3rem;
    background-color: #5EE2BB;
    box-shadow: 0 1px 130px 0 rgba(94, 226, 187, 0.5);
  }
  a {
    all: unset;
  }
</style>
