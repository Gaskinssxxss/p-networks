<template>
  <div class="bg-white text-black font-Host pt-28">
    <!-- Header -->
    <header
      class="fixed top-0 left-0 w-full z-50 bg-white text-black font-Host p-4 md:p-6 border-b-2 md:border-b-4 border-black flex flex-col lg:flex-row justify-between items-center"
    >
      <div class="flex space-x-2 items-center pl-0 lg:pl-4">
        <img class="w-16 md:w-24" src="../assets/p-network.jpg" alt="" />
        <h1
          class="text-lg md:text-2xl font-extrabold uppercase text-center md:text-left"
        >
          Pollacheial Network Tech
        </h1>
      </div>
      <nav
        class="mt-4 md:mt-0 flex flex-wrap justify-center space-x-2 md:space-x-6 pr-0 lg:pr-40"
      >
        <a
          href="#"
          @click.prevent="scrollTo('about')"
          class="hover:bg-black hover:text-white px-2 py-1 border border-black text-sm md:text-base"
          >About</a
        >
        <a
          href="#"
          @click.prevent="scrollTo('services')"
          class="hover:bg-black hover:text-white px-2 py-1 border border-black text-sm md:text-base"
          >Services</a
        >
        <a
          href="#"
          @click.prevent="scrollTo('clients')"
          class="hover:bg-black hover:text-white px-2 py-1 border border-black text-sm md:text-base"
          >Clients</a
        >
        <a
          href="#"
          @click.prevent="scrollTo('contact')"
          class="hover:bg-black hover:text-white px-2 py-1 border border-black text-sm md:text-base"
          >Contact</a
        >
      </nav>
    </header>

    <!-- Hero -->
    <section
      class="px-6 md:px-12 py-16 md:py-32 border-b-2 md:border-b-4 border-black"
      id="home"
    >
      <div class="flex flex-col lg:flex-row justify-between items-center">
        <div class="text-center lg:text-left lg:w-full">
          <h2
            class="text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-extrabold leading-tight uppercase"
          >
            We Build Bold & Secure Digital Experiences
          </h2>
          <div class="mt-6 lg:mt-0 lg:w-1/2 flex sm:hidden justify-center">
            <img
              class="w-3/4 sm:w-2/3 lg:w-full max-w-md"
              src="../assets/tim.png"
              alt=""
            />
          </div>
          <p class="mt-4 sm:mt-6 text-xs sm:text-lg">
            <span class="font-bold">we deliver innovative and sustainable</span>
            digital solutions — from software development and data engineering
            to cybersecurity and networking — enabling businesses and
            institutions to achieve real digital transformation.
          </p>
          <p class="mt-3 sm:mt-4 text-xs sm:text-lg">
            Guided by our vision as a trusted technology partner, we focus on
            <span class="font-bold">security, reliability, and continuity</span>
            while building resilient ecosystems that empower organizations in a
            changing world.
          </p>
          <p class="mt-3 sm:mt-4 text-xs sm:text-lg">
            From <span class="font-bold">IT infrastructure</span> to
            <span class="font-bold">social and environmental research</span>,
            our work ensures measurable impact and lasting value.
          </p>
          <button
            @click="scrollToForm"
            class="mt-6 sm:mt-8 px-4 sm:px-6 py-2 sm:py-3 bg-black text-white border-2 sm:border-4 border-black hover:bg-white hover:text-black transition text-sm sm:text-base"
          >
            Let’s Collaborate With Us
          </button>
        </div>

        <div class="mt-6 lg:mt-0 lg:w-1/2 hidden sm:flex justify-center">
          <img
            class="w-3/4 sm:w-2/3 lg:w-full max-w-md"
            src="../assets/tim.png"
            alt=""
          />
        </div>
      </div>
    </section>

    <!-- Clients -->
    <section
      class="px-6 md:px-12 pt-4 pb-8 border-b-2 md:border-b-4 border-black"
      id="clients"
    >
      <div class="flex items-center space-x-3 mb-6">
        <h3 class="text-2xl sm:text-3xl md:text-4xl font-extrabold uppercase">
          Clients
        </h3>
      </div>
      <div class="overflow-hidden w-full relative">
        <div
          class="marquee whitespace-nowrap flex items-center space-x-12 sm:space-x-32 animate-marquee"
        >
          <template
            v-for="(client, index) in [...clients, ...clients]"
            :key="index"
          >
            <div class="flex items-center space-x-3 sm:space-x-4 min-w-max">
              <img
                :src="client.logo"
                alt="logo"
                class="w-12 h-12 sm:w-16 sm:h-16 lg:w-20 lg:h-20 object-contain"
              />
              <h1 class="text-base sm:text-lg md:text-xl font-bold capitalize">
                {{ client.nama }}
              </h1>
            </div>
          </template>
        </div>
      </div>
    </section>

    <!-- About -->
    <section
      class="p-6 md:p-12 border-b-2 md:border-b-4 border-black"
      id="about"
    >
      <div class="flex items-center space-x-3 mb-6">
        <h3 class="text-2xl sm:text-3xl md:text-4xl font-extrabold uppercase">
          About Us
        </h3>
      </div>
      <div class="space-y-4 max-w-6xl text-base sm:text-lg">
        <p>
          <span class="text-xl sm:text-2xl font-bold"
            >CV. Pollacheial Network Tech</span
          >
          is a technology company focused on providing innovative, secure, and
          sustainable digital solutions.
        </p>
        <p>
          We are committed to delivering professional services that support
          digital transformation, information security, and reliable data and
          system management for business partners and government institutions,
          while adhering to international standards.
        </p>
        <p>
          We position ourselves as a strategic partner capable of delivering
          integrated technology solutions, ranging from software development to
          data analysis, network infrastructure, cybersecurity, as well as
          social and environmental research.
        </p>
      </div>
    </section>

    <!-- Vision -->
    <section
      class="p-6 md:p-12 border-b-2 md:border-b-4 border-black bg-gray-50"
      id="visi"
    >
      <div class="flex items-center space-x-3 mb-6">
        <h3 class="text-2xl sm:text-3xl md:text-4xl font-extrabold uppercase">
          Vision
        </h3>
      </div>
      <p class="text-base sm:text-lg max-w-6xl">
        To become a trusted provider of information technology solutions with
        high standards, making a real contribution to digitalization, security,
        and sustainability across various industries.
      </p>
    </section>

    <!-- Mission -->
    <section
      class="p-6 md:p-12 border-b-2 md:border-b-4 border-black"
      id="misi"
    >
      <div class="flex items-center space-x-3 mb-6">
        <h3 class="text-2xl sm:text-3xl md:text-4xl font-extrabold uppercase">
          Mission
        </h3>
      </div>
      <ul
        class="list-disc list-inside space-y-3 text-base sm:text-lg max-w-6xl"
      >
        <li>
          Delivering industry-standard technology solutions that drive
          efficiency, inclusivity, and sustainability across sectors.
        </li>
        <li>
          Developing smart, adaptive, and reliable data security technologies to
          address evolving cyber threats.
        </li>
        <li>
          Designing and building resilient and scalable digital systems to
          ensure operational continuity for clients.
        </li>
        <li>
          Providing comprehensive system analysis and IT risk management
          services.
        </li>
        <li>
          Offering technical support through system administration and IT
          support services.
        </li>
        <li>
          Continuously innovating through research and development in
          cybersecurity and robust digital infrastructure.
        </li>
      </ul>
    </section>

    <!-- Services -->
    <section
      id="services"
      class="p-6 md:p-12 border-b-2 md:border-b-4 border-black"
    >
      <div class="flex items-center space-x-3 mb-6">
        <h3 class="text-2xl sm:text-3xl md:text-4xl font-extrabold uppercase">
          Services
        </h3>
      </div>
      <div
        class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8"
      >
        <div
          class="p-4 sm:p-6 border-2 sm:border-4 border-black hover:bg-black hover:text-white transition"
        >
          <h4 class="text-lg sm:text-xl md:text-2xl font-bold uppercase mb-3">
            Software Development
          </h4>
          <p class="text-sm sm:text-base">
            Web, Mobile, and Desktop App Development. Building websites,
            e-commerce platforms, Android/iOS apps, and internal management
            systems.
          </p>
        </div>
        <div
          class="p-4 sm:p-6 border-2 sm:border-4 border-black hover:bg-black hover:text-white transition"
        >
          <h4 class="text-lg sm:text-xl md:text-2xl font-bold uppercase mb-3">
            Networking & Infrastructure
          </h4>
          <p class="text-sm sm:text-base">
            LAN/WAN design & installation, enterprise Wi-Fi, telecommunication
            solutions, and IoT for industry, smart buildings, smart agriculture,
            and smart cities.
          </p>
        </div>
        <div
          class="p-4 sm:p-6 border-2 sm:border-4 border-black hover:bg-black hover:text-white transition"
        >
          <h4 class="text-lg sm:text-xl md:text-2xl font-bold uppercase mb-3">
            Data & Database Engineering
          </h4>
          <p class="text-sm sm:text-base">
            Data collection & entry, data engineering, data analysis, data
            science, and database administration (MongoDB, MySQL, PostgreSQL,
            Oracle).
          </p>
        </div>
        <div
          class="p-4 sm:p-6 border-2 sm:border-4 border-black hover:bg-black hover:text-white transition"
        >
          <h4 class="text-lg sm:text-xl md:text-2xl font-bold uppercase mb-3">
            Cybersecurity
          </h4>
          <p class="text-sm sm:text-base">
            Red Team (Offensive), Blue Team (Defensive), incident response &
            recovery.
          </p>
        </div>
        <div
          class="p-4 sm:p-6 border-2 sm:border-4 border-black hover:bg-black hover:text-white transition"
        >
          <h4 class="text-lg sm:text-xl md:text-2xl font-bold uppercase mb-3">
            System Analysis & Risk Engineering
          </h4>
          <p class="text-sm sm:text-base">
            System requirement analysis, risk engineering, and IT system
            optimization for better efficiency and reliability.
          </p>
        </div>
        <div
          class="p-4 sm:p-6 border-2 sm:border-4 border-black hover:bg-black hover:text-white transition"
        >
          <h4 class="text-lg sm:text-xl md:text-2xl font-bold uppercase mb-3">
            Social, Political & Environmental Surveys
          </h4>
          <p class="text-sm sm:text-base">
            Public opinion, political, and environmental surveys conducted using
            scientific methodologies, supported by professional field surveyors.
          </p>
        </div>
        <div
          class="p-4 sm:p-6 border-2 sm:border-4 border-black hover:bg-black hover:text-white transition"
        >
          <h4 class="text-lg sm:text-xl md:text-2xl font-bold uppercase mb-3">
            System Administration & IT Support
          </h4>
          <p class="text-sm sm:text-base">
            Server & system administration, helpdesk & support, backup &
            disaster recovery, and real-time performance monitoring to maintain
            productivity.
          </p>
        </div>
      </div>
    </section>

    <!-- Contact -->
    <section
      class="p-6 md:p-12 border-b-2 md:border-b-4 border-black"
      id="contact"
    >
      <div class="flex items-center space-x-3 mb-6">
        <h3 class="text-2xl sm:text-3xl md:text-4xl font-extrabold uppercase">
          Contact
        </h3>
      </div>
      <div class="flex flex-col lg:flex-row justify-between gap-6">
        <!-- Contact Info -->
        <div class="space-y-4 text-sm sm:text-base lg:w-1/2">
          <p><strong>Address:</strong> Bima City, West Nusa Tenggara</p>
          <p>
            <strong>Email:</strong>
            <a
              href="mailto:pollacheialnetwok@gmail.com"
              class="underline hover:text-gray-600"
            >
              pollacheialnetwork@gmail.com
            </a>
          </p>
          <p><strong>Phone:</strong> 0852-5385-6669 (Daffa)</p>
          <p>
            <a href="https://www.instagram.com/p.networktech/" target="_blank"
              ><p class="hover:text-blue-800">
                <strong>Instagram:</strong> @p.networktech
              </p></a
            >
          </p>
          <p>
            <a
              href="https://www.linkedin.com/company/cv-pollacheial-network-tech/"
              target="_blank"
              ><p class="hover:text-blue-800">
                <strong>LinkedIn:</strong> pollacheialnetwork
              </p></a
            >
          </p>
        </div>
        <!-- Form -->
        <div class="w-full lg:w-1/3">
          <h1 class="pb-4 text-base sm:text-lg font-bold">
            Let’s Collaborate With Us
          </h1>
          <form
            id="contact-form"
            ref="form"
            @submit.prevent="sendEmail"
            class="grid gap-3 sm:gap-4"
          >
            <input
              type="text"
              name="user_name"
              placeholder="Your Name"
              class="border-2 sm:border-4 border-black p-2 sm:p-3 focus:outline-none"
              required
            />
            <input
              type="email"
              name="user_email"
              placeholder="Your Email"
              class="border-2 sm:border-4 border-black p-2 sm:p-3 focus:outline-none"
              required
            />
            <textarea
              name="message"
              placeholder="Your Message"
              rows="5"
              class="border-2 sm:border-4 border-black p-2 sm:p-3 focus:outline-none"
              required
            ></textarea>
            <button
              type="submit"
              class="px-4 sm:px-6 py-2 sm:py-3 bg-black text-white border-2 sm:border-4 border-black hover:bg-white hover:text-black transition text-sm sm:text-base"
            >
              Send
            </button>
          </form>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer
      class="p-4 md:p-6 text-center uppercase font-bold text-sm sm:text-base"
    >
      © 2025 Pollacheial Network Tech — All Rights Reserved
    </footer>
  </div>
</template>

<script setup>
import nusa from "../assets/nusa.jpg";
import dnk from "../assets/dinamika.jpg";
import bimakita from "../assets/bimakita.png";
import pep from "../assets/pep.jpeg";
import untag from "../assets/untag.png";

import { ref, onMounted } from "vue";
import emailjs from "emailjs-com";

const clients = [
  {
    nama: "Mini Olympic Pertamina 2025 (Pertamina EP Sumatra Utara)",
    logo: pep,
  },
  {
    nama: "Treasure Hunt System (Universitas 17 Agustus Surabaya)",
    logo: untag,
  },
  { nama: "Online Travel Agent Booking System (Nusa Vacation)", logo: nusa },
  { nama: "News Portal System (Dinamika Mbojo)", logo: dnk },
  { nama: "News Portal System (Bima Kita)", logo: bimakita },
];

const form = ref(null);

const serviceID = "service_guvuew3";
const templateID = "template_pti5o9k";
const publicKey = "-DEFQdHYri_Q8uiHg";

const sendEmail = () => {
  emailjs.sendForm(serviceID, templateID, form.value, publicKey).then(
    () => {
      alert("Pesan berhasil dikirim! 🚀");
      form.value.reset();
    },
    (error) => {
      console.error("Gagal mengirim pesan:", error);
      alert("Terjadi kesalahan saat mengirim pesan. Coba lagi.");
    }
  );
};

const scrollToForm = () => {
  const el = document.getElementById("contact-form");
  if (el) {
    el.scrollIntoView({ behavior: "smooth" });
  }
};
const scrollTo = (id) => {
  const el = document.getElementById(id);
  if (el) {
    el.scrollIntoView({ behavior: "smooth" });
  }
};
onMounted(() => {
  window.scrollTo({ top: 0, behavior: "smooth" });
});
</script>

<style>
@keyframes marquee {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%);
  }
}

.animate-marquee {
  display: flex;
  width: max-content;
  animation: marquee 25s linear infinite;
}

/* Durasi lebih cepat di HP biar gak kerasa seret */
@media (max-width: 640px) {
  .animate-marquee {
    animation-duration: 12s; /* lebih cepat di layar kecil */
  }
}
</style>
