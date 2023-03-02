<template>

  <main class="px-5">
      <div class="flex justify-center">
        <div class="mr-4 flex flex-col justify-center pb-16">
          <h1 class="text-2xl font-bold mb-2">Mikhail Lystsov</h1>
          
          <span class=" w-[500px]">
            Mikhail Lystsov was born in Russia in the city of Bogdanovich, Ural region, in 1952. In 1970 he successfully graduated highschool and went to the army. 
            He served in the Air Force of the former Czechoslovakia for two years.<br> Mikhail studied law right after the army for a couple of years, 
            but then dropped out due to family reasons and met his future wife. He ended up studying graduating from college summa cum laude in 1978.<br> 
            As for poetry, Mikhail started writing poems in 1971 while being in the army, it became his favorite hobby and a life’s passion. 
            In 2002 he released a book of poems for family and friends.<br> Currently Mikhail is a member of the Union of Writers of Russia in the city of Yekaterinburg. 
            He published his poems in multiple magazines and newspapers, as well as attended various poetry festivals.<br> 
            Mikhail  has a daughter and had a son who died early because of a health condition. He also has three grandchildren.<br> 
            <br>
            Here’s one of his quotes: <i>“All of us, my friends, are poets at heart.”</i>

          </span>
        </div>
        <figure class="pt-3">
          <img class=" rounded-lg" src="@/assets/grandad-photo.jpg" alt="grandad's photo">
          <figcaption> Picture of Mikhail Lystsov</figcaption>
        </figure>
      </div>
    </main>

  <!-- <div class="flex pt-10">
    <h1 class=" text-green-900 text-2xl font-bold">Mikhail Lystsov</h1>
  </div>
  <div class="flex">
    <h2 class="text-green-900 text-xl font-bold">Biography</h2>
  </div>
  <div class="flex">
    <p class=" text-blue-500">
      Text text text
    </p>
  </div> -->
</template>

<style scoped>
  /* Tablet */   
@media all and (min-width: 400px) {
   body {
      grid-template-columns: 200px auto;
      grid-template-rows: 50px 150px 150px 50px;    
      grid-template-areas: 
         "head head" 
         "nav main"
         "aside main"
         "foot foot";
   }
}
</style>

