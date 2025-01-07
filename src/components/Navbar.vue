<template>
    <!-- test text -->
    <nav class="bg-gray-800">
        <div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8">
            <div class="relative flex h-16 items-center justify-between">
                <div class="flex items-center">
                    <!-- <img class="h-8 w-auto" src="https://tailwindui.com/plus/img/logos/mark.svg?color=indigo&shade=500"
                        alt="Your Company" /> -->
                        <a href="#" class="text-white text-xl font-bold">Tawsif <span class="text-[#4cc9f0]">Tamim</span></a>
                </div>
                <div class="hidden sm:flex sm:ml-auto">
                    <div class="flex space-x-4">
                      <a
                        href="#"
                        class="rounded-md px-3 py-2 text-sm font-medium text-[#4cc9f0]"
                        aria-current="page"
                      >
                        Home
                      </a>
                      <a
                        href="#"
                        class="rounded-md px-3 py-2 text-sm font-medium text-gray-300 hover:text-[#4cc9f0] active:text-[#4cc9f0]"
                      >
                        About Me
                      </a>
                      <a
                        href="#"
                        class="rounded-md px-3 py-2 text-sm font-medium text-gray-300 hover:text-[#4cc9f0] active:text-[#4cc9f0]"
                      >
                        Skills
                      </a>
                      <a
                        href="#"
                        class="rounded-md px-3 py-2 text-sm font-medium text-gray-300 hover:text-[#4cc9f0] active:text-[#4cc9f0]"
                      >
                        Projects
                      </a>
                      <a
                        href="#"
                        class="rounded-md px-3 py-2 text-sm font-medium text-gray-300 hover:text-[#4cc9f0] active:text-[#4cc9f0]"
                      >
                        Contact
                      </a>
                    </div>
                  </div>
                  
                  
                <div class="absolute inset-y-0 right-0 flex items-center sm:hidden">
                    <!-- Mobile menu button -->
                    <button type="button"
                        class="relative inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
                        @click="toggleMobileMenu" :aria-expanded="isMobileMenuOpen.toString()">
                        <span class="absolute -inset-0.5"></span>
                        <span class="sr-only">Open main menu</span>
                        <svg v-if="!isMobileMenuOpen" class="block size-6" fill="none" viewBox="0 0 24 24"
                            stroke-width="1.5" stroke="currentColor" aria-hidden="true">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
                        </svg>
                        <svg v-else class="hidden size-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                            stroke="currentColor" aria-hidden="true">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
                        </svg>
                    </button>
                </div>
            </div>
        </div>
        <!-- Mobile menu -->
        <div v-if="isMobileMenuOpen" class="sm:hidden" id="mobile-menu">
            <div class="space-y-1 px-2 pb-3 pt-2">
                <a href="#" class="block rounded-md bg-gray-900 px-3 py-2 text-base font-medium text-white"
                    aria-current="page">
                    Dashboard
                </a>
                <a href="#"
                    class="block rounded-md px-3 py-2 text-base font-medium text-gray-300 hover:bg-gray-700 hover:text-white">
                    Team
                </a>
                <a href="#"
                    class="block rounded-md px-3 py-2 text-base font-medium text-gray-300 hover:bg-gray-700 hover:text-white">
                    Projects
                </a>
                <a href="#"
                    class="block rounded-md px-3 py-2 text-base font-medium text-gray-300 hover:bg-gray-700 hover:text-white">
                    Calendar
                </a>
            </div>
        </div>
    </nav>
</template>

<script>
import { ref } from "vue";

export default {
    setup() {
        const isMobileMenuOpen = ref(false);

        const toggleMobileMenu = () => {
            isMobileMenuOpen.value = !isMobileMenuOpen.value;
        };

        return {
            isMobileMenuOpen,
            toggleMobileMenu,
        };
    },
};
</script>

<style scoped>
.size-6 {
    width: 1.5rem;
    height: 1.5rem;
}
</style>
