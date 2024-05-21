<script>
  import ServiceCard from "./ServiceCard.svelte";
  const serviceData = [
    {
      index: "1",
      title: "Biometrics",
      desc: "Academia-backed & In-house researched State-of-the-Art Face, Fingerprint, and Iris Recognition SDKs. Enable real-time automated Biometric applications on edge devices even without an active internet connection.",
      color: "#34D4AE",
    },
    {
      index: "2",
      title: "Image Analysis",
      desc: "Academia-backed & In-house researched State-of-the-Art Face, Fingerprint, and Iris Recognition SDKs. Enable real-time automated Biometric applications on edge devices even without an active internet connection.",
      color: "#69C0E7",
    },
    {
      index: "3",
      title: "Cross-media Translation",
      desc: "Academia-backed & In-house researched State-of-the-Art Face, Fingerprint, and Iris Recognition SDKs. Enable real-time automated Biometric applications on edge devices even without an active internet connection.",
      color: "#FF9F31",
    },
    {
      index: "4",
      title: "3D Modeling and Design.",
      desc: "Academia-backed & In-house researched State-of-the-Art Face, Fingerprint, and Iris Recognition SDKs. Enable real-time automated Biometric applications on edge devices even without an active internet connection.",
      color: "#FF605F",
    },
  ];
</script>

<div id="services" class="overflow-hidden">
  <div class="flex flex-col w-11/12 mx-auto items-center justify-center pb-10">
    <div class="w-fit my-20">
      <h2 class="text-2xl dark:text-white text-black uppercase my-1">Services</h2>
      <div
        class="bg-gradient-to-r  from-[#0796FF] to-[#91F6FF] rounded-lg mx-auto w-8/12 h-[4px]"
      ></div>
    </div>
    <div class="mb-20 max-w-[1080px]">
      <p class="lg:text-7xl dark:text-white text-black text-center">
        We provide Artificial Intelligence Services
      </p>
    </div>

    <!-- <div class="grid grid-cols-1 lg:grid-cols-2 gap-6 my-10 max-w-[1080px]"> -->
      <ServiceCard data={serviceData} />
    <!-- </div> -->
  </div>
</div>
