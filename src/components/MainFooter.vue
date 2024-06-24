<!-- Qui va la logica del componente (Vue3 + Javascript) -->
<script>
export default {
  name: 'MainFooter',
  data() {
    return {
      email: '',
      message: ''
    };
  },


  /* Così dovrebbe pure funzionare */
  methods: {
    sendMessage() {
      // Logica per l'invio del messaggio
      console.log('Email:', this.email);
      console.log('Message:', this.message);
      // Reset dei campi
      this.email = '';
      this.message = '';
    }
  }
};
</script>



<!-- Qui va il contenuto di questo elemento (HTML) -->
<template>
  <footer class="footer">
    <div class="container">
      <div class="row">
        <!-- Bookings Column -->
        <div class="footer-column">
          <h3>BOOKINGS</h3>
          <address>
            502 New Design Str,<br />
            Melbourne, San Francisco,<br />
            CA 94110, United States Of America Australia<br />
            T: 1-123-456-789<br />
            Email: demo@example.com
          </address>
          <div class="social-icons">
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-facebook-f"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
            <a href="#"><i class="fab fa-youtube"></i></a>
          </div>
        </div>

        <!-- Information Column -->
        <div class="footer-column">
          <h3>INFORMATION</h3>
          <ul>
            <li><a href="#">Product Support</a></li>
            <li><a href="#">Checkout</a></li>
            <li><a href="#">Report Abuse</a></li>
            <li><a href="#">Redeem Voucher</a></li>
            <li><a href="#">Order Status</a></li>
          </ul>
        </div>

        <!-- Support Column -->
        <div class="footer-column">
          <h3>SUPPORT</h3>
          <ul>
            <li><a href="#">Policies & Rules</a></li>
            <li><a href="#">Privacy Policy</a></li>
            <li><a href="#">License Policy</a></li>
            <li><a href="#">My Account</a></li>
            <li><a href="#">Locality</a></li>
          </ul>
        </div>

        <!-- Newsletter Column -->
        <div class="footer-column">
          <h3>NEWSLETTER</h3>
          <form @submit.prevent="sendMessage">
            <input type="email" v-model="email" placeholder="Email" required />
            <textarea v-model="message" placeholder="Message" required></textarea>
            <button type="submit">SEND MESSAGE</button>
          </form>
        </div>
      </div>
    </div>
    <hr>
    <div class="footer-bottom">
      <p>© 2024 All Rights Reserved. Developed By TemplateMela</p>
    </div>
  </footer>
</template>



<!-- Qui va lo stile CSS di questo elemento (CSS) -->
<style lang="scss" scoped>
.footer {
  background-color: #000;
  color: #fff;
  padding: 40px 0;
  font-size: 1.4rem;
}
.container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 20px;
  margin-bottom: 10rem;
}
.row {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  gap: 30px;
}
.footer-column {
  flex: 1;
  min-width: 200px;
  margin: 10px;
}
.footer-column h3 {
  margin-bottom: 20px;
}
.footer-column address,
.footer-column ul,
.footer-column form {
  margin: 0;
  padding: 0;
  list-style: none;
}
.footer-column address {
  line-height: 1.6;
  font-family: "open-sans", sans-serif;
  color: #c5c5c5;
  font-size: 1rem;
}
.footer-column ul li {
  margin-bottom: 5px;
}
.footer-column ul li a {
  color: #c5c5c5;
  text-decoration: none;
  font-family: "open-sans", sans-serif;
  font-size: 1rem;
}
.footer-column ul li a:hover {
  color: #ff8800;
}
.footer-column .social-icons a {
  display: inline-block;
  margin-right: 10px;
  color: #fff;
  text-decoration: none;
}
.footer-column .social-icons a i {
  font-size: .7em;
  margin-right: 1rem;
}
.footer-column form input,
.footer-column form textarea {
  width: 100%;
  padding: 15px;
  margin-bottom: 10px;
  border: 1px solid #3a3a3a;
  background-color: transparent;
  color: #a1a1a1;
  font-size: 1rem;
}
.footer-column form textarea{
  height: 6rem;
}
.footer-column form button {
  padding: 10px 40px;
  background-color: transparent;
  border: 1px solid  #ff8800;
  color: #fff;
  cursor: pointer;
  font-size: .9rem;
  font-weight: 600;
}
.footer-column form button:hover {
  background-color: #ff8800;
}
.footer-bottom {
  text-align: center;
  margin-top: 20px;
  font-family: "open-sans", sans-serif;
  color: #c5c5c5;
  font-size: 1rem;
}

hr{
    border: none;
    height: 2px;
    background-color: rgb(53, 53, 53);
}
</style>