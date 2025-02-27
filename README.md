# utkarsh.page-pjg-
<!doctype html>
<html lang="en" class="scroll-smooth">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1.0" />

    <title>Freebie 64 - Portfolio (Tailwind CSS) by pixelcave</title>

    <meta
      name="description"
      content="Freebie 64 - Portfolio (Tailwind CSS). Check out more at https://pixelcave.com"
    />
    <meta name="author" content="pixelcave" />

    <!-- Icons -->
    <link
      rel="icon"
      href="https://cdn.pixelcave.com/favicon.svg"
      sizes="any"
      type="image/svg+xml"
    />
    <link
      rel="icon"
      href="https://cdn.pixelcave.com/favicon.png"
      type="image/png"
    />

    <!-- Inter web font from bunny.net (GDPR compliant) -->
    <link rel="preconnect" href="https://fonts.bunny.net" />
    <link
      href="https://fonts.bunny.net/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap"
      rel="stylesheet"
    />

    <!-- Tailwind CSS Play CDN (mainly for development/testing purposes) -->
    <script src="https://cdn.tailwindcss.com?plugins=forms,typography,aspect-ratio"></script>

    <!-- Tailwind CSS v3 Configuration -->
    <script>
      const defaultTheme = tailwind.defaultTheme;
      const colors = tailwind.colors;
      const plugin = tailwind.plugin;

      tailwind.config = {
        darkMode: "class",
        theme: {
          extend: {
            fontFamily: {
              sans: ["Inter", ...defaultTheme.fontFamily.sans],
            },
          },
        },
      };
    </script>

    <!-- Alpine.js -->
    <script
      defer
      src="https://unpkg.com/alpinejs@3.x.x/dist/cdn.min.js"
    ></script>

    <!-- Alpine.js (x-cloak - https://alpinejs.dev/directives/cloak) -->
    <style>
      [x-cloak] {
        display: none !important;
      }
    </style>
  </head>
  <body class="antialiased">
    <!-- Page Container -->
    <div
      x-data="{
        darkMode: false,
        toggleDarkMode() {
          this.darkMode = ! this.darkMode;

          // Toggle dark class on html element
          if (this.darkMode) {
            document.body.parentNode.classList.add('dark');
          } else {
            document.body.parentNode.classList.remove('dark');
          }
        }
      }"
      class="min-h-dvh min-w-80 bg-white text-zinc-800 dark:bg-zinc-950 dark:text-zinc-100"
    >
      <!-- Page Content -->
      <main
        id="page-content"
        class="mx-auto flex max-w-6xl flex-auto flex-col px-4 pb-4 lg:px-8 lg:pb-8"
      >
        <!-- Main Header -->
        <header
          id="page-header"
          class="flex flex-none items-center justify-between py-7"
        >
          <div class="flex items-center gap-2">
            <!-- Logo -->
            <a
              href="javascript:void(0)"
              class="text-2xl font-thin tracking-widest hover:text-purple-600 active:opacity-75 dark:hover:text-purple-400"
            >
              UTKARSH
            </a>
            <!-- END Logo -->

            <!-- Toggle Dark Mode -->
            <button
              x-on:click="toggleDarkMode()"
              type="button"
              class="relative inline-flex size-9 items-center justify-center text-zinc-600 hover:opacity-75 dark:text-zinc-400"
            >
              <div
                x-cloak
                x-show="!darkMode"
                x-transition:enter="transition ease-out duration-150"
                x-transition:enter-start="opacity-0 rotate-180"
                x-transition:enter-end="opacity-100 rotate-0"
                x-transition:leave="transition ease-in duration-100"
                x-transition:leave-start="opacity-100 rotate-0"
                x-transition:leave-end="opacity-0 rotate-180"
                class="absolute inset-0 flex items-center justify-center"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke-width="1.5"
                  stroke="currentColor"
                  class="hi-outline hi-sun inline-block size-5"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M12 3v2.25m6.364.386-1.591 1.591M21 12h-2.25m-.386 6.364-1.591-1.591M12 18.75V21m-4.773-4.227-1.591 1.591M5.25 12H3m4.227-4.773L5.636 5.636M15.75 12a3.75 3.75 0 1 1-7.5 0 3.75 3.75 0 0 1 7.5 0Z"
                  />
                </svg>
              </div>
              <div
                x-cloak
                x-show="darkMode"
                x-transition:enter="transition ease-out duration-150"
                x-transition:enter-start="opacity-0 rotate-180"
                x-transition:enter-end="opacity-100 rotate-0"
                x-transition:leave="transition ease-in duration-100"
                x-transition:leave-start="opacity-100 rotate-0"
                x-transition:leave-end="opacity-0 rotate-180"
                class="absolute inset-0 flex items-center justify-center"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke-width="1.5"
                  stroke="currentColor"
                  class="hi-outline hi-moon inline-block size-5"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M21.752 15.002A9.72 9.72 0 0 1 18 15.75c-5.385 0-9.75-4.365-9.75-9.75 0-1.33.266-2.597.748-3.752A9.753 9.753 0 0 0 3 11.25C3 16.635 7.365 21 12.75 21a9.753 9.753 0 0 0 9.002-5.998Z"
                  />
                </svg>
              </div>
            </button>
            <!-- END Toggle Dark Mode -->
          </div>
          <div class="flex items-center gap-4">
            <!-- Nav -->
            <nav class="flex items-center gap-6">
              <a
                href="#projects"
                class="text-sm font-medium decoration-purple-600 decoration-2 underline-offset-8 hover:text-black hover:underline dark:decoration-purple-400 dark:hover:text-white"
              >
                Projects
              </a>
              <a
                href="#contact"
                class="text-sm font-medium decoration-purple-600 decoration-2 underline-offset-8 hover:text-black hover:underline dark:decoration-purple-400 dark:hover:text-white"
              >
                Hire me
              </a>
            </nav>
            <!-- END Nav -->
          </div>
        </header>
        <!-- END Main Header -->

        <!-- Main Content -->
        <div class="grid grid-cols-1 gap-6 md:grid-cols-12">
          <!-- Photo -->
          <div class="col-span-1 md:col-span-5">
            <div class="aspect-h-1 aspect-w-1">
              <img
                src=<img jsname="kSDGid" class="bn6k9b" aria-hidden="true" alt="" role="none" 
             <img
                src="utkarsh-photo.jpg"
                alt="Utkarsh Portfolio"
                class="rounded-xl object-cover"
             />
            </div>
          </div>
          <!-- END Photo -->

          <!-- Intro -->
          <div
            class="relative col-span-1 flex flex-col overflow-hidden rounded-xl bg-zinc-100 p-12 dark:bg-zinc-900 md:col-span-7"
          >
            <div
              aria-hidden="true"
              class="absolute -left-20 -top-20 size-48 rounded-full bg-yellow-500 blur-2xl"
            ></div>
            <div
              aria-hidden="true"
              class="absolute -right-10 -top-10 size-64 rounded-full bg-orange-300 blur-3xl"
            ></div>
            <div
              aria-hidden="true"
              class="absolute inset-0 bg-yellow-100/50 backdrop-blur-md dark:bg-yellow-900/75"
            ></div>
            <div class="relative mt-auto">
              <h1 class="text-4xl font-medium text-black dark:text-white">
                "Hi there, I'm Utkarsh Barnwal!"
              </h1>
              <h2 class="mt-3 leading-relaxed text-zinc-900 dark:text-zinc-200">
                "I'm a passionate Web Developer currently pursuing my BCA, equipped with strong problem-solving skills and a creative mindset. I specialize in crafting modern, responsive, and user-friendly websites using HTML, CSS, JavaScript, and various front-end technologies.
                
                With a keen interest in UI/UX design, I focus on building interactive web applications that enhance user experience. My expertise extends to developing seamless, high-performance websites with clean code and efficient functionality.
                
                I believe in continuous learning and staying updated with the latest web trends and technologies. Through my projects, I demonstrate my ability to design, develop, and optimize websites that not only look great but also function flawlessly. My goal is to create innovative digital experiences that make an impact!"
              </h2>
            </div>
          </div>
          <!-- END Intro -->

          <!-- Projects -->
          <a
            id="projects"
            href="javascript:void(0)"
            class="group relative col-span-1 overflow-hidden rounded-xl bg-zinc-100 p-6 hover:bg-zinc-200/75 active:bg-zinc-200 dark:bg-zinc-900 dark:hover:bg-zinc-800/75 dark:active:bg-zinc-800 md:col-span-4"
          >
            <div
              class="absolute right-6 top-6 scale-0 opacity-0 transition duration-75 ease-out group-hover:scale-100 group-hover:opacity-100"
              aria-hidden="true"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="currentColor"
                class="hi-solid hi-arrow-small-right inline-block size-6"
              >
                <path
                  fill-rule="evenodd"
                  d="M3.75 12a.75.75 0 0 1 .75-.75h13.19l-5.47-5.47a.75.75 0 0 1 1.06-1.06l6.75 6.75a.75.75 0 0 1 0 1.06l-6.75 6.75a.75.75 0 1 1-1.06-1.06l5.47-5.47H4.5a.75.75 0 0 1-.75-.75Z"
                  clip-rule="evenodd"
                />
              </svg>
            </div>
            <h3 class="text-lg font-medium text-zinc-950 dark:text-zinc-50">
              Wev dev
            </h3>
            <h4 class="text-sm text-zinc-600 dark:text-zinc-400">This month</h4>
            <div
              class="aspect-h-3 aspect-w-4 mt-10 transition duration-150 ease-out group-hover:scale-105"
            >
              <img
                src=https://cdn-employer-wp.arc.dev/wp-content/uploads/2022/04/good-software-developer-1128x635.jpg
                alt="Project 1"
                class="rounded-xl object-cover"
              />
            </div>
          </a>
          <a
            href="javascript:void(0)"
            class="group relative col-span-1 overflow-hidden rounded-xl bg-zinc-100 p-6 hover:bg-zinc-200/75 active:bg-zinc-200 dark:bg-zinc-900 dark:hover:bg-zinc-800/75 dark:active:bg-zinc-800 md:col-span-4"
          >
            <div
              class="absolute right-6 top-6 scale-0 opacity-0 transition duration-75 ease-out group-hover:scale-100 group-hover:opacity-100"
              aria-hidden="true"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="currentColor"
                class="hi-solid hi-arrow-small-right inline-block size-6"
              >
                <path
                  fill-rule="evenodd"
                  d="M3.75 12a.75.75 0 0 1 .75-.75h13.19l-5.47-5.47a.75.75 0 0 1 1.06-1.06l6.75 6.75a.75.75 0 0 1 0 1.06l-6.75 6.75a.75.75 0 1 1-1.06-1.06l5.47-5.47H4.5a.75.75 0 0 1-.75-.75Z"
                  clip-rule="evenodd"
                />
              </svg>
            </div>
            <h3 class="text-lg font-medium text-zinc-950 dark:text-zinc-50">
             Python
            </h3>
            <h4 class="text-sm text-zinc-600 dark:text-zinc-400">This month</h4>
            <div
              class="aspect-h-3 aspect-w-4 mt-10 transition duration-150 ease-out group-hover:scale-105"
            >
              <img
                src=https://blog.eduonix.com/wp-content/uploads/2018/09/Scientific-Python-Scipy.jpg
                alt="Project 2"
                class="rounded-xl object-cover"
              />
            </div>
          </a>
          <a
            href="javascript:void(0)"
            class="group relative col-span-1 overflow-hidden rounded-xl bg-zinc-100 p-6 hover:bg-zinc-200/75 active:bg-zinc-200 dark:bg-zinc-900 dark:hover:bg-zinc-800/75 dark:active:bg-zinc-800 md:col-span-4"
          >
            <div
              class="absolute right-6 top-6 scale-0 opacity-0 transition duration-75 ease-out group-hover:scale-100 group-hover:opacity-100"
              aria-hidden="true"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="currentColor"
                class="hi-solid hi-arrow-small-right inline-block size-6"
              >
                <path
                  fill-rule="evenodd"
                  d="M3.75 12a.75.75 0 0 1 .75-.75h13.19l-5.47-5.47a.75.75 0 0 1 1.06-1.06l6.75 6.75a.75.75 0 0 1 0 1.06l-6.75 6.75a.75.75 0 1 1-1.06-1.06l5.47-5.47H4.5a.75.75 0 0 1-.75-.75Z"
                  clip-rule="evenodd"
                />
              </svg>
            </div>
            <h3 class="text-lg font-medium text-zinc-950 dark:text-zinc-50">
              <HTML:5>
                C++
            </h3>
              
            <h4 class="text-sm text-zinc-600 dark:text-zinc-400">This month</h4>
            <div
              class="aspect-h-3 aspect-w-4 mt-10 transition duration-150 ease-out group-hover:scale-105"
            >
              <img
                src=https://assets.codeguru.com/uploads/2003/02/C-tutorials-420x420.jpg
                alt="Project 3"
                class="rounded-xl object-cover"
              />
            </div>
          </a>
          <a
            href="javascript:void(0)"
            class="group relative col-span-1 overflow-hidden rounded-xl bg-zinc-100 p-6 hover:bg-zinc-200/75 active:bg-zinc-200 dark:bg-zinc-900 dark:hover:bg-zinc-800/75 dark:active:bg-zinc-800 md:col-span-4"
          >
            <div
              class="absolute right-6 top-6 scale-0 opacity-0 transition duration-75 ease-out group-hover:scale-100 group-hover:opacity-100"
              aria-hidden="true"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="currentColor"
                class="hi-solid hi-arrow-small-right inline-block size-6"
              >
                <path
                  fill-rule="evenodd"
                  d="M3.75 12a.75.75 0 0 1 .75-.75h13.19l-5.47-5.47a.75.75 0 0 1 1.06-1.06l6.75 6.75a.75.75 0 0 1 0 1.06l-6.75 6.75a.75.75 0 1 1-1.06-1.06l5.47-5.47H4.5a.75.75 0 0 1-.75-.75Z"
                  clip-rule="evenodd"
                />
              </svg>
            </div>
            <h3 class="text-lg font-medium text-zinc-950 dark:text-zinc-50">
              Power BI
            </h3>
            <h4 class="text-sm text-zinc-600 dark:text-zinc-400">Last month</h4>
            <div
              class="aspect-h-3 aspect-w-4 mt-10 transition duration-150 ease-out group-hover:scale-105"
            >
              <img
                src="https://d17thj9kqp1mkn.cloudfront.net/strapi-assets-tech_a34b41e7f9.jpg">
            
            </div>
          </a>
          <a
            href="javascript:void(0)"
            class="group relative col-span-1 overflow-hidden rounded-xl bg-zinc-100 p-6 hover:bg-zinc-200/75 active:bg-zinc-200 dark:bg-zinc-900 dark:hover:bg-zinc-800/75 dark:active:bg-zinc-800 md:col-span-4"
          >
            <div
              class="absolute right-6 top-6 scale-0 opacity-0 transition duration-75 ease-out group-hover:scale-100 group-hover:opacity-100"
              aria-hidden="true"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="currentColor"
                class="hi-solid hi-arrow-small-right inline-block size-6"
              >
                <path
                  fill-rule="evenodd"
                  d="M3.75 12a.75.75 0 0 1 .75-.75h13.19l-5.47-5.47a.75.75 0 0 1 1.06-1.06l6.75 6.75a.75.75 0 0 1 0 1.06l-6.75 6.75a.75.75 0 1 1-1.06-1.06l5.47-5.47H4.5a.75.75 0 0 1-.75-.75Z"
                  clip-rule="evenodd"
                />
              </svg>
            </div>
            <h3 class="text-lg font-medium text-zinc-950 dark:text-zinc-50">
              Data structure
            </h3>
            <h4 class="text-sm text-zinc-600 dark:text-zinc-400">Last month</h4>
            <div
              class="aspect-h-3 aspect-w-4 mt-10 transition duration-150 ease-out group-hover:scale-105"
            >
              <img
                src=https://media2.dev.to/dynamic/image/width=1000,height=420,fit=cover,gravity=auto,format=auto/https%3A%2F%2Fthepracticaldev.s3.amazonaws.com%2Fi%2Fsrnvrd7vfeeq5qpxnabq.png
                alt="Project 5"
                class="rounded-xl object-cover"
              />
            </div>
          </a>
          <a
            href="javascript:void(0)"
            class="group relative col-span-1 overflow-hidden rounded-xl bg-zinc-100 p-6 hover:bg-zinc-200/75 active:bg-zinc-200 dark:bg-zinc-900 dark:hover:bg-zinc-800/75 dark:active:bg-zinc-800 md:col-span-4"
          >
            <div
              class="absolute right-6 top-6 scale-0 opacity-0 transition duration-75 ease-out group-hover:scale-100 group-hover:opacity-100"
              aria-hidden="true"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="currentColor"
                class="hi-solid hi-arrow-small-right inline-block size-6"
              >
                <path
                  fill-rule="evenodd"
                  d="M3.75 12a.75.75 0 0 1 .75-.75h13.19l-5.47-5.47a.75.75 0 0 1 1.06-1.06l6.75 6.75a.75.75 0 0 1 0 1.06l-6.75 6.75a.75.75 0 1 1-1.06-1.06l5.47-5.47H4.5a.75.75 0 0 1-.75-.75Z"
                  clip-rule="evenodd"
                />
              </svg>
            </div>
            <h3 class="text-lg font-medium text-zinc-950 dark:text-zinc-50">
              Graphic design
            </h3>
            <h4 class="text-sm text-zinc-600 dark:text-zinc-400">Last month</h4>
            <div
              class="aspect-h-3 aspect-w-4 mt-10 transition duration-150 ease-out group-hover:scale-105"
            >
              <img
                src=<img width="540" height="457" src="https://www.netleafinfosoft.com/our-blog/wp-content/uploads/2019/10/Graphic-Design-Services-in-Gurgaon.jpg" class="attachment-post-thumbnail size-post-thumbnail wp-post-image" alt="Graphic Design Services in Gurgaon" decoding="async" srcset="https://www.netleafinfosoft.com/our-blog/wp-content/uploads/2019/10/Graphic-Design-Services-in-Gurgaon.jpg 540w, https://www.netleafinfosoft.com/our-blog/wp-content/uploads/2019/10/Graphic-Design-Services-in-Gurgaon-473x400.jpg 473w" sizes="(max-width: 540px) 100vw, 540px">
            
            </div>
          </a>
          <!-- END Projects -->

          <!-- Contact -->
          <div
            id="contact"
            class="relative col-span-1 flex flex-col overflow-hidden rounded-xl bg-zinc-100 px-12 py-20 dark:bg-zinc-900 md:col-span-12"
          >
            <div
              aria-hidden="true"
              class="absolute -left-20 -top-20 size-48 rounded-full bg-pink-300 blur-2xl"
            ></div>
            <div
              aria-hidden="true"
              class="absolute -bottom-48 -right-48 size-96 rounded-full bg-indigo-200 blur-2xl dark:bg-indigo-400/50"
            ></div>
            <div
              aria-hidden="true"
              class="absolute -right-48 -top-48 size-96 rounded-full bg-purple-200 blur-3xl dark:bg-purple-400/50"
            ></div>
            <div
              aria-hidden="true"
              class="absolute inset-0 bg-purple-100/50 backdrop-blur-md dark:bg-purple-900/75"
            ></div>
            <div class="relative mx-auto mt-auto max-w-md">
              <h2 class="text-4xl font-medium text-black dark:text-white">
                Get in touch
              </h2>
              <h3 class="mt-3 leading-relaxed text-zinc-900 dark:text-zinc-200">
                Looking for a creative partner for your next project? I'm
                currently available for freelance work and would love to hear
                about your ideas. Whether you need branding, web design, or
                print materials, let's collaborate to bring your vision to life.
              </h3>
              <form onsubmit="return false;" class="mt-10 w-full space-y-6">
                <div class="space-y-2">
                  <label for="name" class="text-sm font-medium">Name</label>
                  <input
                    type="text"
                    id="name"
                    name="name"
                    class="block w-full rounded-lg border border-white px-5 py-3 leading-6 placeholder-zinc-500 focus:border-purple-500 focus:ring focus:ring-purple-500/50 dark:border-purple-950 dark:bg-purple-950 dark:placeholder-zinc-400 dark:focus:border-purple-500"
                  />
                </div>
                <div class="space-y-2">
                  <label for="email" class="text-sm font-medium">Email</label>
                  <input
                    type="email"
                    id="email"
                    name="email"
                    class="block w-full rounded-lg border border-white px-5 py-3 leading-6 placeholder-zinc-500 focus:border-purple-500 focus:ring focus:ring-purple-500/50 dark:border-purple-950 dark:bg-purple-950 dark:placeholder-zinc-400 dark:focus:border-purple-500"
                  />
                </div>
                <div class="space-y-2">
                  <label for="message" class="text-sm font-medium"
                    >Message</label
                  >
                  <textarea
                    id="message"
                    name="message"
                    rows="6"
                    class="block w-full rounded-lg border border-white px-5 py-3 leading-6 placeholder-zinc-500 focus:border-purple-500 focus:ring focus:ring-purple-500/50 dark:border-purple-950 dark:bg-purple-950 dark:placeholder-zinc-400 dark:focus:border-purple-500"
                  ></textarea>
                </div>
                <button
                  type="submit"
                  class="inline-flex w-full items-center justify-center gap-2 rounded-lg border border-purple-700 bg-purple-700 px-5 py-3 text-sm font-semibold leading-6 text-white hover:border-purple-600 hover:bg-purple-600 hover:text-white focus:ring focus:ring-purple-400/50 active:border-purple-700 active:bg-purple-700 dark:focus:ring-purple-400/90 lg:w-auto"
                >
                  <span>Send Message</span>
                </button>
              </form>
            </div>
          </div>
          <!-- END Contact -->

          <!-- Footer -->
          <footer
            class="flex flex-col gap-6 py-7 text-center text-sm md:col-span-12 md:flex-row-reverse md:justify-between md:gap-0 md:text-left"
          >
            <nav class="flex items-center justify-center gap-4">
              <a
                href="javascript:void(0)"
                class="text-zinc-400 hover:text-zinc-800 dark:hover:text-white"
              >
                <svg
                  class="bi bi-twitter-x inline-block size-5"
                  xmlns="http://www.w3.org/2000/svg"
                  fill="currentColor"
                  viewBox="0 0 16 16"
                  aria-hidden="true"
                >
                  <path
                    d="M12.6.75h2.454l-5.36 6.142L16 15.25h-4.937l-3.867-5.07-4.425 5.07H.316l5.733-6.57L0 .75h5.063l3.495 4.633L12.601.75Zm-.86 13.028h1.36L4.323 2.145H2.865l8.875 11.633Z"
                  />
                </svg>
              </a>
              <a
                href="javascript:void(0)"
                class="text-zinc-400 hover:text-[#1877f2]"
              >
                <svg
                  class="icon-facebook inline-block size-5"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 24 24"
                  fill="currentColor"
                >
                  <path
                    d="M9 8H6v4h3v12h5V12h3.642L18 8h-4V6.333C14 5.378 14.192 5 15.115 5H18V0h-3.808C10.596 0 9 1.583 9 4.615V8z"
                  ></path>
                </svg>
              </a>
              <a
                href="javascript:void(0)"
                class="text-zinc-400 hover:text-[#405de6]"
              >
                <svg
                  class="icon-instagram inline-block size-5"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 24 24"
                  fill="currentColor"
                >
                  <path
                    d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.052.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98C8.333 23.986 8.741 24 12 24c3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zM12 16a4 4 0 110-8 4 4 0 010 8zm6.406-11.845a1.44 1.44 0 100 2.881 1.44 1.44 0 000-2.881z"
                  ></path>
                </svg>
              </a>
              <a
                href="javascript:void(0)"
                class="text-zinc-400 hover:text-[#333] dark:hover:text-zinc-50"
              >
                <svg
                  class="icon-github inline-block size-5"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 24 24"
                  fill="currentColor"
                >
                  <path
                    d="M12 0C5.374 0 0 5.373 0 12c0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23A11.509 11.509 0 0112 5.803c1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576C20.566 21.797 24 17.3 24 12c0-6.627-5.373-12-12-12z"
                  ></path>
                </svg>
              </a>
              <a
                href="javascript:void(0)"
                class="text-zinc-400 hover:text-[#ea4c89]"
              >
                <svg
                  class="icon-dribbble inline-block size-5"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 24 24"
                  fill="currentColor"
                >
                  <path
                    d="M12 0C5.372 0 0 5.373 0 12s5.372 12 12 12 12-5.373 12-12S18.628 0 12 0zm9.885 11.441c-2.575-.422-4.943-.445-7.103-.073a42.153 42.153 0 00-.767-1.68c2.31-1 4.165-2.358 5.548-4.082a9.863 9.863 0 012.322 5.835zm-3.842-7.282c-1.205 1.554-2.868 2.783-4.986 3.68a46.287 46.287 0 00-3.488-5.438A9.894 9.894 0 0112 2.087c2.275 0 4.368.779 6.043 2.072zM7.527 3.166a44.59 44.59 0 013.537 5.381c-2.43.715-5.331 1.082-8.684 1.105a9.931 9.931 0 015.147-6.486zM2.087 12l.013-.256c3.849-.005 7.169-.448 9.95-1.322.233.475.456.952.67 1.432-3.38 1.057-6.165 3.222-8.337 6.48A9.865 9.865 0 012.087 12zm3.829 7.81c1.969-3.088 4.482-5.098 7.598-6.027a39.137 39.137 0 012.043 7.46c-3.349 1.291-6.953.666-9.641-1.433zm11.586.43a41.098 41.098 0 00-1.92-6.897c1.876-.265 3.94-.196 6.199.196a9.923 9.923 0 01-4.279 6.701z"
                  ></path>
                </svg>
              </a>
            </nav>
            <div class="text-zinc-500 dark:text-zinc-400/80">
              <span class="font-medium">UTKARSH BARNWAL</span> © 
              <span x-text="new Date().getFullYear()"></span>
            </div>
          </footer>
          <!-- END Footer -->
        </div>
        <!-- END Main Content -->
      </main>
      <!-- END Page Content -->
    </div>
    <!-- END Page Container -->
  </body>
</html>

