<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import {
  faSquareEnvelope,
  faMobileAlt,
} from '@fortawesome/free-solid-svg-icons';
import { faLinkedinIn } from '@fortawesome/free-brands-svg-icons';

export default {
  components: {
    FontAwesomeIcon,
  },
  data() {
    return {
      nome: 'Leonardo Guimarães',
      email: 'leonardo.cientistadedados@gmail.com',
      telefone: '+55 (61) 99666-8080',
      linkedin: 'https://www.linkedin.com/feed/',
      envelopeIcon: faSquareEnvelope,
      mobileIcon: faMobileAlt,
      linkedinIcon: faLinkedinIn,
    };
  },
};
</script>

<template>
  <div class="app">
    <div class="content">
      <div class="header">
        <header>
          <img
            src="/images/WhatsApp Image 2024-01-30 at 09.59.20.jpeg"
            alt="minha foto"
            class="profile-picture"
          />
          <p>{{ nome }}</p>
        </header>
      </div>
      <main>
        <section>
          <h2>Desenvolvedor Front-End</h2>
          <p>{{ descricao }}</p>
        </section>
        <section>
          <ul>
            <li><font-awesome-icon :icon="envelopeIcon" /> {{ email }}</li>
            <li>
              <font-awesome-icon :icon="mobileIcon" />
              {{ telefone }}
            </li>
            <li>
              <font-awesome-icon :icon="linkedinIcon" />
              <a :href="linkedin">{{ linkedin }}</a>
            </li>
          </ul>
        </section>
      </main>
    </div>
  </div>
</template>

<style>
/* Estilos CSS */
@import url('https://fonts.googleapis.com/css?family=Muli&display=swap');

body {
  background-color: steelblue;
}

.app {
  padding: 20px;
  font-family: 'Muli';
  background-color: #f7f7f7;
  border-radius: 10px;
}

header {
  text-align: center;
  margin-bottom: 20px;
}

.profile-picture {
  width: 150px;
  height: 150px;
  border-radius: 50%; /* Para tornar a imagem redonda */
  object-fit: cover; /* Para garantir que a imagem cubra todo o espaço disponível */
  margin-bottom: 10px;
}

h1 {
  font-size: 2.5rem;
  margin-bottom: 5px;
}

p {
  font-size: 1.5rem;
  color: #000000;
  text-align: center;
}

main section {
  margin-bottom: 20px;
}

h2 {
  font-size: 1.8rem;
  text-align: center;
  color: #000000;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  margin-bottom: 5px;
  color: black;
  text-align: left;
  font-size: 0.9rem;
}

a {
  color: #007bff;
  text-decoration: none;
}

a:hover {
  text-decoration: none;
  border-radius: 5px;
}
</style>
