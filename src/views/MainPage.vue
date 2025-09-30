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
          >Tentang</a
        >
        <a
          href="#"
          @click.prevent="scrollTo('services')"
          class="hover:bg-black hover:text-white px-2 py-1 border border-black text-sm md:text-base"
          >Layanan</a
        >
        <a
          href="#"
          @click.prevent="scrollTo('clients')"
          class="hover:bg-black hover:text-white px-2 py-1 border border-black text-sm md:text-base"
          >Klien</a
        >
        <a
          href="#"
          @click.prevent="scrollTo('contact')"
          class="hover:bg-black hover:text-white px-2 py-1 border border-black text-sm md:text-base"
          >Kontak</a
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
            class="text-xl sm:text-4xl md:text-5xl font-extrabold leading-tight uppercase"
          >
            Merancang sistem Digital yang berorientasi pada solusi, ketangguhan, dan mampu meneyelsaikan masalah anda.
          </h2>
          <div class="mt-6 lg:mt-0 lg:w-1/2 flex sm:hidden justify-center">
            <img
              class="w-3/4 sm:w-2/3 lg:w-full max-w-md"
              src="../assets/tim.png"
              alt=""
            />
          </div>
          <p class="mt-4 sm:mt-6 text-xs sm:text-lg">
            <span class="font-bold">Kami menghadirkan solusi digital inovatif dan berkelanjutan</span>
            — mulai dari pengembangan perangkat lunak, rekayasa data, hingga keamanan siber dan jaringan — memungkinkan bisnis dan institusi mencapai transformasi digital nyata.
          </p>
          <p class="mt-3 sm:mt-4 text-xs sm:text-lg">
            Dipandu oleh visi kami sebagai mitra teknologi terpercaya, kami berfokus pada
            <span class="font-bold">keamanan, keandalan, dan kesinambungan</span>
            dalam membangun ekosistem tangguh yang memberdayakan organisasi di dunia yang terus berubah.
          </p>
          <p class="mt-3 sm:mt-4 text-xs sm:text-lg">
            Dari <span class="font-bold">infrastruktur TI</span> hingga
            <span class="font-bold">penelitian sosial dan lingkungan</span>,
            pekerjaan kami memastikan dampak yang terukur dan nilai yang berkelanjutan.
          </p>
          <button
            @click="scrollToForm"
            class="mt-6 sm:mt-8 px-4 sm:px-6 py-2 sm:py-3 bg-black text-white border-2 sm:border-4 border-black hover:bg-white hover:text-black transition text-sm sm:text-base"
          >
            Ayo Berkolaborasi Dengan Kami
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
          Klien
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
          Tentang Kami
        </h3>
      </div>
      <div class="space-y-4 max-w-6xl text-base sm:text-lg">
        <p>
          <span class="text-xl sm:text-2xl font-bold"
            >CV. Pollacheial Network Tech</span
          >
          adalah perusahaan teknologi yang berfokus pada penyediaan solusi digital inovatif, aman, dan berkelanjutan.
        </p>
        <p>
          Kami berkomitmen memberikan layanan profesional yang mendukung transformasi digital, keamanan informasi, serta manajemen data dan sistem yang andal bagi mitra bisnis dan institusi pemerintah dengan standar internasional.
        </p>
        <p>
          Kami memposisikan diri sebagai mitra strategis yang mampu memberikan solusi teknologi terintegrasi, mulai dari pengembangan perangkat lunak, analisis data, infrastruktur jaringan, keamanan siber, hingga penelitian sosial dan lingkungan.
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
          Visi
        </h3>
      </div>
      <p class="text-base sm:text-lg max-w-6xl">
        Menjadi penyedia solusi teknologi informasi terpercaya dengan standar tinggi, serta memberikan kontribusi nyata dalam digitalisasi, keamanan, dan keberlanjutan di berbagai industri.
      </p>
    </section>

    <!-- Mission -->
    <section
      class="p-6 md:p-12 border-b-2 md:border-b-4 border-black"
      id="misi"
    >
      <div class="flex items-center space-x-3 mb-6">
        <h3 class="text-2xl sm:text-3xl md:text-4xl font-extrabold uppercase">
          Misi
        </h3>
      </div>
      <ul
        class="list-disc list-inside space-y-3 text-base sm:text-lg max-w-6xl"
      >
        <li>
          Menyediakan solusi teknologi berstandar industri yang mendorong efisiensi, inklusivitas, dan keberlanjutan lintas sektor.
        </li>
        <li>
          Mengembangkan teknologi keamanan data yang cerdas, adaptif, dan andal untuk menghadapi ancaman siber yang terus berkembang.
        </li>
        <li>
          Merancang dan membangun sistem digital yang tangguh dan skalabel guna memastikan kesinambungan operasional klien.
        </li>
        <li>
          Memberikan analisis sistem dan layanan manajemen risiko TI yang komprehensif.
        </li>
        <li>
          Menyediakan dukungan teknis melalui administrasi sistem dan layanan bantuan TI.
        </li>
        <li>
          Terus berinovasi melalui penelitian dan pengembangan dalam bidang keamanan siber dan infrastruktur digital yang kuat.
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
          Layanan
        </h3>
      </div>
      <div
        class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8"
      >
        <div
          class="p-4 sm:p-6 border-2 sm:border-4 border-black hover:bg-black hover:text-white transition"
        >
          <h4 class="text-lg sm:text-xl md:text-2xl font-bold uppercase mb-3">
            Pengembangan Perangkat Lunak
          </h4>
          <p class="text-sm sm:text-base">
            Pengembangan aplikasi Web, Mobile, dan Desktop. Membangun situs web, platform e-commerce, aplikasi Android/iOS, serta sistem manajemen internal.
          </p>
        </div>
        <div
          class="p-4 sm:p-6 border-2 sm:border-4 border-black hover:bg-black hover:text-white transition"
        >
          <h4 class="text-lg sm:text-xl md:text-2xl font-bold uppercase mb-3">
            Jaringan, Iot & Infrastruktur Jaringan
          </h4>
          <p class="text-sm sm:text-base">
            Desain & instalasi LAN/WAN, Wi-Fi enterprise, solusi telekomunikasi, dan IoT untuk industri, gedung pintar, pertanian pintar, dan kota pintar.
          </p>
        </div>
        <div
          class="p-4 sm:p-6 border-2 sm:border-4 border-black hover:bg-black hover:text-white transition"
        >
          <h4 class="text-lg sm:text-xl md:text-2xl font-bold uppercase mb-3">
            Rekayasa Data & Basis Data
          </h4>
          <p class="text-sm sm:text-base">
            Pengumpulan & entri data, rekayasa data, analisis data, data science, dan administrasi basis data (MongoDB, MySQL, PostgreSQL, Oracle).
          </p>
        </div>
        <div
          class="p-4 sm:p-6 border-2 sm:border-4 border-black hover:bg-black hover:text-white transition"
        >
          <h4 class="text-lg sm:text-xl md:text-2xl font-bold uppercase mb-3">
            Keamanan Siber
          </h4>
          <p class="text-sm sm:text-base">
            Red Team (Ofensif), Blue Team (Defensif), respon insiden & pemulihan.
          </p>
        </div>
        <div
          class="p-4 sm:p-6 border-2 sm:border-4 border-black hover:bg-black hover:text-white transition"
        >
          <h4 class="text-lg sm:text-xl md:text-2xl font-bold uppercase mb-3">
            Analisis Sistem & Rekayasa Risiko
          </h4>
          <p class="text-sm sm:text-base">
            Analisis kebutuhan sistem, rekayasa risiko, dan optimasi sistem TI untuk efisiensi dan keandalan yang lebih baik.
          </p>
        </div>
        <div
          class="p-4 sm:p-6 border-2 sm:border-4 border-black hover:bg-black hover:text-white transition"
        >
          <h4 class="text-lg sm:text-xl md:text-2xl font-bold uppercase mb-3">
            Survei Sosial, Politik & Lingkungan
          </h4>
          <p class="text-sm sm:text-base">
            Survei opini publik, politik, dan lingkungan menggunakan metodologi ilmiah, didukung surveyor lapangan profesional.
          </p>
        </div>
        <div
          class="p-4 sm:p-6 border-2 sm:border-4 border-black hover:bg-black hover:text-white transition"
        >
          <h4 class="text-lg sm:text-xl md:text-2xl font-bold uppercase mb-3">
            Administrasi Sistem & Dukungan TI
          </h4>
          <p class="text-sm sm:text-base">
            Administrasi server & sistem, layanan helpdesk & dukungan, backup & pemulihan bencana, serta pemantauan kinerja real-time untuk menjaga produktivitas.
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
          Kontak
        </h3>
      </div>
      <div class="flex flex-col lg:flex-row justify-between gap-6">
        <!-- Contact Info -->
        <div class="space-y-4 text-sm sm:text-base lg:w-1/2">
          <p><strong>Alamat:</strong> Kota Bima, Nusa Tenggara Barat</p>
          <p>
            <strong>Email:</strong>
            <a
              href="mailto:pollacheialnetwok@gmail.com"
              class="underline hover:text-gray-600"
            >
              pollacheialnetwork@gmail.com
            </a>
          </p>
          <p><strong>Telepon:</strong> 0852-5385-6669 (Daffa)</p>
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
            Ayo Berkolaborasi Dengan Kami
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
              placeholder="Nama Anda"
              class="border-2 sm:border-4 border-black p-2 sm:p-3 focus:outline-none"
              required
            />
            <input
              type="email"
              name="user_email"
              placeholder="Email Anda"
              class="border-2 sm:border-4 border-black p-2 sm:p-3 focus:outline-none"
              required
            />
            <textarea
              name="message"
              placeholder="Pesan Anda"
              rows="5"
              class="border-2 sm:border-4 border-black p-2 sm:p-3 focus:outline-none"
              required
            ></textarea>
            <button
              type="submit"
              class="px-4 sm:px-6 py-2 sm:py-3 bg-black text-white border-2 sm:border-4 border-black hover:bg-white hover:text-black transition text-sm sm:text-base"
            >
              Kirim
            </button>
          </form>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer
      class="p-4 md:p-6 text-center uppercase font-bold text-sm sm:text-base"
    >
      © 2025 Pollacheial Network Tech — Hak Cipta Dilindungi
    </footer>
  </div>
</template>

<script setup>
import nusa from "../assets/nusa.jpg";
import dnk from "../assets/dinamika.jpg";
import bimakita from "../assets/bimakita.png";
import pep from "../assets/pep.jpeg";
import untag from "../assets/untag.png";
import piongsejahtera from "../assets/piongsejahtera.png"

import { ref, onMounted } from "vue";
import emailjs from "emailjs-com";

const clients = [
  {
    nama: "Mini Olympic Pertamina 2025 (Pertamina EP Sumatra Barat)",
    logo: pep,
  },
  {
    nama: "Sistem & Game Treasure Hunt (Universitas 17 Agustus Surabaya)",
    logo: untag,
  },
  { nama: "Infrastruktur & Penyedia Jaringan Wifi (Piong Sejahtera)", logo: piongsejahtera },
  { nama: "Sistem Booking Online Agen Travel (Nusa Vacation)", logo: nusa },
  { nama: "Portal Berita (Dinamika Mbojo)", logo: dnk },
  { nama: "Portal Berita (Bima Kita)", logo: bimakita },
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
    animation-duration: 20s; /* lebih cepat di layar kecil */
  }
}
</style>
