<script setup lang="ts">
useHead({
  title: 'FAQ',
})

const faqs: FaqItem[] = [
  {
    question:
      'Bahasa apa yang harus digunakan untuk Cover Letter, CV, dan Self-Introduction Video?',
    answer:
      'Bahasa yang digunakan bebas, Bahasa Indonesia atau Bahasa Inggris tidak masalah.',
  },
  {
    question: 'Bagaimana isi Self-Introduction Video?',
    answer:
      'Harus memperlihatkan diri, perkenalkan diri, alasan mau menjadi asprak, buat sekreatif mungkin. Pastikan account Instagram tidak di-private ya.',
  },
  {
    question: 'Isi Cover Letter?',
    answer:
      'Sesuai dengan isi cover letter formal pada umumnya, seperti saat akan melamar suatu pekerjaan.',
  },
  {
    question: 'Mata kuliah apa saja yang harus minimal B?',
    answer:
      'Tidak ada ketentuan mata kuliah apa saja, yang penting IPK diatas 3.00. Persyaratan nilai mata kuliah tertentu minimal B hanya digunakan ketika memilih mata kuliah apa yang diajarkan nanti.',
  },
  {
    question: 'Test coding? Apa yang harus dipersiapkan?',
    answer:
      'Tidak rumit, test ini untuk melihat sejauh mana kalian menyelesaikan suatu permasalahan dasar dengan logika sederhana. Untuk apa yang harus dipersiapkan, bagaimana prosesnya akan diinformasikan kepada pendaftar.',
  },
  {
    question: 'Upload jawaban online assessment kemana?',
    answer:
      'Upload di web ini, nanti akan muncul button upload di halaman timeline recruitment pada tanggal 23 Januari 2024 dimulai pukul 13.00 WIB hingga 18.00 WIB.',
  },
]

const contacts = [
  'Rizky Ramadhan Sudjarmono (Line ID : rizky09oktober2004)',
  'Muhammad Naufal Nur Ramadhan (LINE ID : tanyasamasatpam)',
]
</script>

<template>
  <main>
    <div class="h-screen bg-[#2b2526]" flex="~ col">
      <div
        class="justify-center p-12 h-fit xl:p-24 grow"
        flex="~ col"
        xl="h-full"
        style="
          background-image: var(--bg-image);
          background-repeat: no-repeat;
          background-size: cover;
        "
      >
        <span text="2rem md:4rem [#fdca32]" font="sans bold"
          >Frequently Asked Questions</span
        >
        <div class="flex flex-col mt-4 text-white divide-y divide-gray-700">
          <FAQCard v-for="(faq, i) in faqs" :key="i" :faq="faq" />
        </div>

        <div class="w-full mt-12 mb-4 border border-white"></div>

        <div class="flex flex-col">
          <span class="text-[#fdca32] text-lg font-bold"
            >Further Questions?</span
          >
          <span text="base white"> Drop your questions to : </span>
          <ul class="mt-1 ml-6 text-white list-disc">
            <li>{{ contacts[0] }}</li>
            <li>{{ contacts[1] }}</li>
          </ul>
        </div>
      </div>
      <Footer />
    </div>
  </main>
</template>

<style scoped>
main {
  --bg-image: url('/bg/faq-narrow.png');
}

@media (min-width: 1024px) {
  main {
    --bg-image: url('/bg/faq-wide.png');
  }
}
</style>
