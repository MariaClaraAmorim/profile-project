<script lang="ts">
  import { onMount } from "svelte";

  const THEME_KEY = "theme";

  // Tema automático baseado na preferência do usuário
  onMount(() => {
    const theme = window.localStorage.getItem(THEME_KEY);

    const prefersDarkTheme = window.matchMedia(
      "(prefers-color-scheme: dark)"
    ).matches;

    if (theme === "dark" || (theme === null && prefersDarkTheme)) {
      setTheme("dark");
    } else {
      setTheme("light")
    }
  });

  // Função para alterar o tema
  const setTheme = (theme: string) => {
    const oldClasses = document.documentElement.classList.value;
    if (oldClasses) document.documentElement.classList.remove(oldClasses);
    document.documentElement.classList.add(theme);
    window.localStorage.setItem(THEME_KEY, theme)
  };
</script>

<div class="flex gap-1">
  <button
    class="bg-gray-100 dark:bg-gray-800 text-gray-900 dark:text-gray-400 border-none cursor-pointe px-2"
    on:click={() => setTheme("dark")}
  >
    Dark
  </button>

  <button
    class="bg-gray-900 dark:bg-gray-100 text-gray-400 dark:text-gray-900 border-none cursor-pointer px-2"
    on:click={() => setTheme("light")}
  >
    Light
  </button>
</div>
