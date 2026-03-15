<script lang="ts">
  import "iconify-icon";
  interface repository {
    name: string;
    desc: string;
    url: string;
  }

  const repos: repository[] = [
    {
      name: "progoat",
      desc: "LLM-powered CLI for programming education. Generate structured courses on any topic and solve coding exercises directly from your terminal.",
      url: "https://github.com/minotto165/progoat",
    },
    {
      name: "EatenDLP",
      desc: "A Fluent UI YouTube downloader built with WPF and iNKORE.UI.WPF.Modern. Provides a clean, modern interface for content downloads.",
      url: "https://github.com/minotto165/EatenDLP",
    },
    {
      name: "FluentVRC",
      desc: "A Fluent UI launcher for VRChat.",
      url: "https://github.com/minotto165/FluentVRC",
    },
  ];

  let repo: repository;
</script>

<div class="min-h-screen w-screen flex justify-center bg-linear-to-b from-[#00090C] to-[#001016] py-8 px-8 sm:py-12">
  <div class="content w-xl 2xl:w-3xl flex flex-col gap-8 sm:gap-12">
    <div class="relative rounded-2xl border-[#34454B80] border-2 overflow-hidden shadow-lg shadow-[#A7C9D410] h-50 sm:h-80">
      <img alt="banner" src="/banner.png" class="w-full h-full object-cover" />
      <div class="absolute inset-0 bg-linear-to-b from-[#00000020] to-[#00151d]"></div>
      <div class="absolute inset-0 flex justify-between items-end p-4 sm:p-6">
        <div class="flex flex-raw items-center gap-4 sm:gap-6">
          <img alt="logo" src="/logo.svg" class="h-8 sm:h-12 pl-2 drop-shadow-[#DAF6FF50] drop-shadow-lg" />
          <div class="flex flex-col items-start justify-end">
            <p class="text-[#D7EDF4] font-plex text-3xl sm:text-4xl font-medium drop-shadow-[#DAF6FF50] drop-shadow-lg">Minotto</p>
            <p class="text-[#B3DBE8] font-plex text-sm sm:text-xl font-light -mt-1 drop-shadow-[#DAF6FF50] drop-shadow-lg">Designer / Programmer</p>
          </div>
        </div>
        <a href="https://github.com/minotto165" target="_blank">
          <button class="h-12 w-12 sm:w-30 rounded-lg border-[#34454B80] border-2 flex items-center justify-center gap-1 shadow-2xs bg-[#000e1390] hover:bg-[#00080a95] hover:-translate-y-0.5 active:scale-98 duration-100 px-1">
            <iconify-icon icon="hugeicons:github" class="text-[#D7EDF4] text-xl"></iconify-icon>
            <p class="text-[#D7EDF4] font-plex text-base hidden sm:block">Github</p>
          </button>
        </a>
      </div>
    </div>
    <div class="flex flex-col gap-2 sm:gap-4">
      <h1 class="text-[#A7C9D4] font-plex font-semibold text-4xl sm:text-5xl drop-shadow-xl drop-shadow-[#DAF6FF30]">About Me</h1>
      <p class="text-[#C5D4D9] font-plex text-lg">Developer interested in Go, CLI tools, and open source. Also exploring creative tools like After Effects, FL Studio, and Figma.</p>
    </div>
    <div class="flex flex-col gap-4 sm:gap-6">
      <h1 class="text-[#A7C9D4] font-plex font-semibold text-4xl sm:text-5xl drop-shadow-xl drop-shadow-[#DAF6FF30]">Projects</h1>
      {#each repos as repo}
        <div class="flex flex-col gap-2 sm:gap-3">
          <div class="flex gap-2 sm:gap-3 items-center">
            <h2 class="text-[#EDF8FB] font-plex text-2xl sm:text-3xl">{repo.name}</h2>
            <!-- svelte-ignore a11y_consider_explicit_label -->
            <a href={repo.url} target="_blank" class="relative top-1">
              <iconify-icon icon="hugeicons:github" class="text-[#D7EDF4] text-xl sm:text-2xl"></iconify-icon>
            </a>
          </div>
          <p class="text-[#C5D4D9] font-plex text-sm sm:text-base">{repo.desc}</p>
        </div>
      {/each}
    </div>
  </div>
</div>
