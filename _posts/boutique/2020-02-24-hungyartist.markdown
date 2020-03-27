---
layout: post
title:  "Hungy Artist, Acrylique sur toile,40x40 cm, 2020."
date:   2020-02-01 19:57:21
preview: /img/hungry_artist.jpg
category: boutique
---

![Picture 1](/img/hungry_artist.jpg) 


Hungy Artist, Acrylique sur toile,40x40 cm, 2020.


<div id="paypal-button-container"></div>

<script>
    //paypal.Buttons().render('#paypal-button-container');
    
  paypal.Buttons({
    createOrder: function(data, actions) {
      // This function sets up the details of the transaction, including the amount and line item details.
      return actions.order.create({
        purchase_units: [{
          amount: {
            value: '75'
          }
        }]
      });
    },
    onApprove: function(data, actions) {
      // This function captures the funds from the transaction.
      return actions.order.capture().then(function(details) {
        // This function shows a transaction success message to your buyer.
        alert('Transaction completed by ' + details.payer.name.given_name);
      });
    }
  }).render('#paypal-button-container');
</script>


