<template>
  <div class="flex items-center gap-4" @click="onclic">
    <!-- Icono TEMA -->
    <div
      class="cursor-pointer"
      id="theme-toggle"
      aria-label="Toggle theme"
      role="button"
    >
      <div class="min-w-14 max-w-14 bg-[#223344] rounded-3xl flex p-1 gap-2">
        <div class="dark:bg-yellow-50 rounded-full min-w-5">
          <img src="/resources/Moon_fill.svg" alt="Moon Icon" />
        </div>
        <div class="bg-yellow-50 rounded-full min-w-5 dark:opacity-0">
          <img src="/resources/Sun_fill.svg" alt="Sun Icon" />
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>

    
function onclic() {
    const themeToggle = document.getElementById("theme-toggle");
  const htmlElement = document.documentElement;
    console.log("hola")
  if (htmlElement.classList.contains("dark")) {
    htmlElement.classList.remove("dark");
    localStorage.setItem("theme", "light");
  } else {
    htmlElement.classList.add("dark");
    localStorage.setItem("theme", "dark");
  }
}




</script>
