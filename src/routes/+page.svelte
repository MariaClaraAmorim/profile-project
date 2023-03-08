<script>
  let name = "Maria Clara Amorim";
</script>

<section class="bg-white dark:bg-gray-900">
  <div class="relative flex">
    <div class="min-h-screen lg:w-1/3" />
    <div
      class="hidden w-3/4 min-h-screen bg-gray-100 dark:bg-gray-800 lg:block"
    />

    <div
      class="container flex flex-col justify-center w-full min-h-screen px-6 py-10 mx-auto lg:absolute lg:inset-x-0"
    >
      <div class="mt-10 lg:mt-20 lg:flex lg:items-center">
        <img
          class="object-cover object-center w-full lg:w-[32rem] rounded-lg h-96"
          src="https://api.dicebear.com/5.x/adventurer/svg?seed=Cookie"
          alt=""
        />

        <div class="mt-8 lg:px-10 lg:mt-0">
          <h1
            class="text-2xl font-semibold text-gray-800 dark:text-white lg:w-72"
          >
            Hi, {name} here, nice to meet you!
          </h1>

          <p class="max-w-lg mt-6 text-gray-500 dark:text-gray-400">
            Graduated in the technical course in Informatics, at the Federal
            Institute of Bahia (IFBA) - Campus Barreiras. I currently work with
            Front-End development at Dantas Eletro/Dantas Bikes.
          </p>

          <h3 class="mt-6 text-lg font-medium text-blue-500">{name}</h3>
          <p class="text-gray-600 dark:text-gray-300">Developer Front-End</p>
        </div>
      </div>
    </div>
  </div>
</section>
