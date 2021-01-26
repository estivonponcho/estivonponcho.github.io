---
layout: posts
title:  "Welcome to Dayton Ridge Golf Club Restaurant and Bar!"
date:   2021-01-25 19:30:56 -0600
categories: jekyll update
---
Established in 2000, Dayton Ridge Golf Club has become a fixture in the Ottawa, IL area. We pair the spirit of good drinking with food golf and a friendly atmosphere. Which makes for one deliciously unique experience. Come visit us to golf, drink and eat!



Check out our [Facebook Page][facebook] for more info!

[facebook]: https://www.facebook.com/daytonridgegolf/

<div id="smart-button-container">
      <div style="text-align: center;">
        <div id="paypal-button-container"></div>
      </div>
    </div>
  <script src="https://www.paypal.com/sdk/js?client-id=sb&currency=USD" data-sdk-integration-source="button-factory"></script>
  <script>
    function initPayPalButton() {
      paypal.Buttons({
        style: {
          shape: 'rect',
          color: 'gold',
          layout: 'vertical',
          label: 'paypal',
          
        },

        createOrder: function(data, actions) {
          return actions.order.create({
            purchase_units: [{"description":"test","amount":{"currency_code":"USD","value":1}}]
          });
        },

        onApprove: function(data, actions) {
          return actions.order.capture().then(function(details) {
            alert('Transaction completed by ' + details.payer.name.given_name + '!');
          });
        },

        onError: function(err) {
          console.log(err);
        }
      }).render('#paypal-button-container');
    }
    initPayPalButton();
  </script>