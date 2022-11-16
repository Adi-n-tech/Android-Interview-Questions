**1) How we can implement Razor pay in Android?**

Steps for Integration - 

1. We need to install Razor pay SDK from the Android Project 
2. Initialize Razor Pay SDK with the Preload Checkout Method and the Razor Pay Key ID (Key ID can be for TEST mode or LIVE mode)
3. Using the server-side Razor Pay API, construct an order ID by passing the required amount and currency type params.
4. Pass the generated order ID while Initiating the payment and checkout display forms. It include the required amount and currency params also some other optional params, such as (email, contact, name, theme. color, etc.)
5. After the user makes a payment using any method, we will receive a response callback indicating whether it was successful or failure. In the case of success, we will receive razorpay payment id, razorpay order id, and razorpay signature; in the event of a failure, we will receive ERROR CODE.
6. Using the razorpay signature id param on the server, we can confirm the payment.
7. Successful payment entries with capture status are visible in the Razor pay dashboard.

This is how we can implement razor pay.
