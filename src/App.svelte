<script>
  import Nav from './lib/Nav.svelte'
  import Info from './lib/Info.svelte'
  import Footer from './lib/footer/Footer.svelte';
  import Button from './lib/Button.svelte';
  import Works from './lib/works/Works.svelte';
  import { Route } from 'tinro';
  import OrderInfo from './lib/OrderInfo.svelte';
  import { ShoppingCartSimple } from 'phosphor-svelte';
</script>

<a id="top"></a>
<div id="content">
  <Nav />
  <Route path="/">
    <Info />
    <div class="button">
      <Button text={"view my services"} icon={ShoppingCartSimple}/>
    </div>
    <Works />
  </Route>
  <Route path="/order">
    <OrderInfo />
  </Route>
  <Footer />
</div>

<style>
  :root {
    background-color: #101010;
    color: white;
    margin: 0;
    padding: 0;
  }
  #content {
    max-width: 960px;
    margin: auto;
    background-color: black;
    background-image: url(gradient.svg);
    background-position: 50% 100%;
    background-repeat: no-repeat;
    background-size: 100%, 10%;
    -webkit-font-smoothing: antialiased;
    font-smooth: never;
  }
  .button {
    margin-left: 100px;
  }
</style>