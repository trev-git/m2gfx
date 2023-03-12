<script lang="ts">
  import Button from "$lib/Button.svelte";
  import { ClipboardText, PlusCircle, ShoppingCart } from "phosphor-svelte";
  import InputBox from "./InputBox.svelte";
</script>

<div class="content">
  <div class="title-layout">
    <div class="title-text-layout">
      <h1>Contact</h1>
      <p class="normal-text">If you have your idea ready for a project, get in touch with me right away, and I’ll give you an estimate of the cost in a moment’s notice!</p>
      <p class="normal-text">You can alternatively email me at:</p>
      <a class="normal-text email" href="mailto:m2.matt2e2@gmail.com">m2.matt2e2@gmail.com</a>
    </div>
    <div class="_2rem-layout">
      <Button icon={ShoppingCart} link={"/order"} text={"pricings"} />
      <Button icon={ClipboardText} link={"/terms"} text={"read the terms"} style={"outlined"} />
    </div>
  </div>
</div>

<div class="content layouted">
  <form id="contact-form" action="submit" class="grid">
    <InputBox placeholder={"john.doe@gmail.com"} type={"email"} label={"Subject *"}/>
    <InputBox placeholder={"Write a short, general overview of your project."} label={"Title *"}/>
    <InputBox placeholder={"Give me a few details of what your project is about, what I should know etc."} multiline={true} label={"Project Details *"}/>
  </form>
  <div class="form-button">
    <Button icon={PlusCircle} text={"Submit request"} type={"submit"} style={"secondary"} form={"contact-form"} link={"/lmao"} />
  </div>
</div>

<style>
  .email {
    color: var(--accent-two);
  }
  .email:hover {
    text-decoration: underline;
  }
  .grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    column-gap: 4rem;
    row-gap: 2rem;
  }
  #contact-form {
    margin-bottom: 2rem;
    width: 100%;
  }
  .content:nth-child(2) {
    margin-top: 0;
  }
  #contact-form:valid + .form-button {
    opacity: 1;
    transition: opacity .2s;
  }
  #contact-form:invalid + .form-button {
    opacity: 0.5;
    transition: opacity .2s;
  }
</style>