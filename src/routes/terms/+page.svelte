<script lang="ts">
  import MetaTitle from "$lib/MetaTitle.svelte";
  import Term from "./Term.svelte";
  import Button from "$lib/Button.svelte";
  import { PaperPlaneTilt, ShoppingCart } from "phosphor-svelte";

  type termPoints = { number: number, title: string, items: string[], display?: boolean};

  const points: termPoints[] = [
    {
      number: 1,
      title: "Preamble",
      items: [
        "By purchasing my services (designs / video work / projects), you automatically agree to the following conditions.",
        "Please read this entirely and carefully. The commission process may not continue if you do not agree to these terms.",
        "If you are not comfortable with my Terms of Service and / or are not willing to agree to the conditions, you may not request a commission.",
        "NFT usage is strictly forbidden.",
        "If you have any questions, please contact me either via email (m2.matt2e2@gmail.com) or through Twitter DM (@mattsquare_)."
      ],
      display: true
    },
    {
      number: 2,
      title: "Copyright",
      items: [
        "M2 disclaims any responsibility for copyright issues. By providing material (sounds effects, artwork, fonts etc.) for use in delivering the service, the client guarantees ownership of the correct licences for the material in question.",
        "The client does not have the right to repurpose, redistribute or edit any of the commissioned products unless I provide the client with an Extended Licence, further reading in the Licencing section.",
        "The client does not have the right to claim the commission as their own work, even after purchasing an Extended Licence and editing the design.",
        "If the client purchases any editable source files (.psd, .fig, .aep files), they are authorised to modify the product but not repurpose or redistribute it unless I provide the client with an Extended Licence."
      ]
    },
    {
      number: 3,
      title: "General Client Terms",
      items: [
        "You, the Client, will be expected to first read my ToS and understand my general Commission Prices.",
        "You, the Client, may display my work on external sites as long as it is visibly credited and linked back to me.",
        "You may use the Artwork for personal use including but not limited to: avatars, phone or computer wallpapers, and personal website / profile displays.",
        "You reserve the right to print or create an otherwise physical reproduction of the Artwork as long as it is for your PERSONAL use only (i.e. NOT for retail).",
        "You may NOT use the Artwork for redistribution or external projects, commercial or non-commercial (for example: merchandise, advertising etc.) unless otherwise discussed.",
        "Clients that fall under the above category are permitted to include signatures and / or watermarks indicating the Artwork is my intellectual property. Credit in some form is required."
      ]
    },
    {
      number: 4,
      title: "Confidentiality & Publishing",
      items: [
        "Once the payment / initial payment has gone through, an automatic Non-Disclosure Agreement is assumed, in which case M2 will not disclose to any person(s) any information about the project without specified written permission from the client, or unless the information has already been publicly disclosed by the client.",
        "On contacting for inquiries on commissioning, M2 will also not disclose any information about the project, material sent over by the customer, debut information etc. unless already publicly disclosed by the customer.",
        "This clause will survive cancellation of the commission and any other agreement and licence."
      ]
    },
    {
      number: 5,
      title: "Commercial Use",
      items: [
        "If the client states in advance that the project commissioned will be used commercially (that includes merchandise, web design, advertising, etc.), pricing will be discussed upfront with the client and will abide by the Payment terms described in the Terms of Service.",
        "Also refer to the terms on Licensing."
      ]
    },
    {
      number: 6,
      title: "Commissioning",
      items: [
        "Upon reaching out and discussing project details with the client, the client may be added to the Active order queue or a Client Waitlist.",
        "Clients in the Waitlist are not required to pay any amount upfront, and will be notified via the method of communication mutually agreed upon when they can be added to the Active order queue.",
        "A client will be added to the Active order queue after payment goes through, and will be provided with an estimated waiting time, after which the client will be notified via the method of communication mutually agreed upon when work on the project has started.",
        "Clients in the Waitlist to be added to the queue have 1-2 days to settle payment for their project, after which the order will get automatically cancelled.",
        "The client in the queue may inquire about progress on their order at any given time, or will be notified personally to provide feedback to a draft or to issue modifications to their end product.",
        "Upon failure to provide feedback when notified, the order will be put on hold.",
        "The client will be removed from the queue once the order is completed, a refund has been issued, or if the order has been cancelled.",
        "Any client in the Waitlist may be removed from the list upon their request, but their placement in the Waitlist may not be reinstated."
      ]
    },
    {
      number: 7,
      title: "Payment",
      items: [
        "Payments or other fees are to be invoiced through Stripe, PayPal, or other payment methods, with prices calculated from $USD.",
        "Understand that the order price will include a small administrative fee based on the method used.",
        "Payments are to be made fully upfront. Orders over $300 USD can be paid either fully upfront or half upfront, half after the client’s approval of the work ordered."
      ]
    },
    {
      number: 8,
      title: "Delivery",
      items: [
        "Orders will be delivered archived in .zip files via email.",
        "The client may ask after order delivery, to receive some delivered products in other file formats (such as .png, .svg, .mp4)."
      ]
    },
    {
      number: 9,
      title: "Refunds",
      items: [
        "Full refunds can be issued at any time before the client has been notified that work on the project has started.",
        "Refunds may sometimes take in between 1-2 weeks time to be issued.",
        "Refunds will NOT include the administrative fee paid at the beginning of the process.",
        "For orders over $300 (paid half upfront, half after the client’s approval of the work ordered), refunds after work on the project has started can be issued for the first half of the price paid.",
        "For orders paid fully upfront, refunds can be issued at 75% original price after work on the client’s project has started.",
        "Upon delivery of the order, refunds may not be issued."
      ]
    }
  ];
</script>

<MetaTitle title="ToS" />
<div class="content grid">
  <div class="title-layout">
    <div class="title-text-layout">
      <div class="order-status-layout">
        <h1>Terms of Service</h1>
      </div>
      <p class="normal-text">
        These are the terms you automatically agree to when commissioning from me. Read carefully and fully, as the commission process may not continue if you disagree with these terms.
      </p>
      <p class="normal-text">
        As the services provided are non-subscription, this document may be subject to change without notice.
      </p>
    </div>
    <div class="_2rem-layout">
      <Button text={"order"} icon={ShoppingCart} link={"/order"}/>
      <Button text={"contact"} icon={PaperPlaneTilt} style={"outlined"} link={"/contact"}/>
    </div>
  </div>
</div>

{#each points as point}
  <div class="content layouted">
    <Term number={point.number} title={point.title} items={point.items} paragraphDisplay={point.display}/>
  </div>
{/each}

<div class="content layouted">
  <div class="terms">
    <div class="title">
      <h2 class="number bold-text">//10</h2>
      <h2 class="title bold-text">Licensing</h2>
    </div>
    <div class="points">

      <div class="license">
        <p class="bold-text">Personal License:</p>
        <ul class="gap">
          <li class="normal-text">By default orders are delivered for Personal Use. The client may:
            <ul>
              <li class="normal-text">Use any commissioned product on Twitch, YouTube for monetized content;</li>
              <li class="normal-text">Use any commissioned product on other Social media platforms such as Discord, Twitter, Instagram, TikTok, etc.</li>
            </ul>
          </li>
          <li class="normal-text">The client may not:
            <ul>
              <li>Use any commissioned product on merchandise or prints;</li>
              <li>Resell any commissioned product;</li>
              <li>Redistribute and / or Edit any commissioned product.</li>
            </ul>
          </li>
        </ul>
      </div>

      <div class="license">
        <p class="bold-text">Commercial License</p>
        <ul class="gap">
          <li class="normal-text">Orders to be used commercially are to be discussed via the contact methods or via video call (Zoom / Discord), and will have pricing settled with the client based on the project and use case.</li>
          <li class="normal-text">Beyond the use cases permitted by the Personal License, the client may:
            <ul>
              <li>Use commissioned products on merchandise or prints;</li>
              <li>Resell commissioned products;</li>
              <li>Redistribute and / or Edit commissioned products.</li>
            </ul>
          </li>
        </ul>
      </div>

      <div class="license">
        <p class="bold-text">Extended License</p>
        <ul class="gap">
          <li class="normal-text">The client may ask for an Extended License for 100% original price, which beyond the use cases permitted by the Personal Licence, the client may:
            <ul>
              <li class="normal-text">Redistribute and / or Edit any commissioned products.</li>
            </ul>
          </li>
        </ul>
      </div>

    </div>
  </div>
</div>

<div class="content layouted">
  <h2>Thank you for reading!</h2>
  <p class="normal-text">Thank you for taking the time to read the terms! Not many do it, but you can be safer in knowing exactly what to expect from placing your order!</p>
</div>

<div class="content layouted">
  <p class="bold-text">Have you decided on what you're getting?</p>
  <div class="_2rem-layout">
    <Button icon={PaperPlaneTilt} link={"/contact"} text={"get in touch"}/>
    <Button icon={ShoppingCart} link={"/order"} text={"pricing"} style={"outlined"}/>
  </div>
</div>

<style>
  .title {
    display: inline-flex;
    gap: 1rem;
    align-items: center;
  }
  h2 {
    font-family: 'Poppins';
    font-weight: 900;
    font-size: 2rem;
  }
  .number {
    font-family: 'StretchProV2';
  }
  ul {
    padding-left: 1rem;
    margin: 0;
  }
  .points {
    margin-top: 1.5rem;
  }
  .license {
    margin-bottom: 1.5rem;
  }
  .license > p {
    margin-bottom: 1rem;
  }
  .gap {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }
</style>