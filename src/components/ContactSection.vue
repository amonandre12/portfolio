<template>
  <section id="contact">
    <div class="contact-container">
      <h2>Contactez-moi</h2>
      <form @submit.prevent="sendEmail">
        <div class="form-group">
          <label for="name">Nom</label>
          <input type="text" id="name" v-model="form.name" placeholder="Votre nom" required />
        </div>

        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" v-model="form.email" placeholder="Votre email" required />
        </div>

        <div class="form-group">
          <label for="message">Message</label>
          <textarea id="message" v-model="form.message" placeholder="Votre message" required></textarea>
        </div>

        <button type="submit" class="btn">Envoyer</button>
      </form>

      <div v-if="message" class="success-message">
        {{ message }}
      </div>
    </div>
  </section>
</template>

<script>
import emailjs from "emailjs-com";
import { ref } from "vue";

export default {
  setup() {
    const form = ref({
      name: "",
      email: "",
      message: "",
    });

    const message = ref("");

    const sendEmail = () => {
      if (form.value.name && form.value.email && form.value.message) {
        emailjs
          .send(
            "service_mulg44g", 
            "template_a9f82vj", 
            form.value,
            "TtuUosp4VqJnJtLwv" 
          )
          .then(() => {
            message.value = "Merci pour votre message ! Je vous répondrai très bientôt.";
            form.value = { name: "", email: "", message: "" };

            setTimeout(() => {
              message.value = "";
            }, 5000);
          })
          .catch(() => {
            message.value = "Erreur lors de l'envoi.";
          });
      } else {
        message.value = "Veuillez remplir tous les champs.";
      }
    };

    return { form, message, sendEmail };
  },
};
</script>

<style scoped>
.contact-container {
  padding: 80px 30px;
  text-align: center;
}

form {
  display: flex;
  flex-direction: column;
  gap: 20px;
  max-width: 600px;
  margin: auto;
}

.form-group {
  display: flex;
  flex-direction: column;
  text-align: left;
}

input,
textarea {
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
  outline: none;
}

textarea {
  height: 150px;
}

.btn {
  background: #00dfc0;
  color: #333;
  padding: 10px 20px;
  border: none;
  cursor: pointer;
  transition: background 0.3s ease;
}

.btn:hover {
  background: #00b89c;
}

.success-message {
  margin-top: 20px;
  color: green;
  font-weight: bold;
}
</style>