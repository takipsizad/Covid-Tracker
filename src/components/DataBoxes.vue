<template>
    <div class="gird md:grid-cols-2 gap-4">
        <div class="shadow-md bg-pink-100 p-10 text-center rounded">
            <h3 class="text-3xl text-pink-900 font-bold mb-4">
                Cases
            </h3>

          <div class="text-2xl mb-4">
              <span class="font-bold">New: </span>
              {{ stats.NewConfirmed }}
          </div>
          <div class="text-2xl mb-4">
              <span class="font-bold">Total: </span>
              {{ stats.TotalConfirmed }}
          </div>

        </div>
        <div class="shadow-md bg-pink-300 p-10 text-center rounded">
            <h3 class="text-3xl text-pink-900 font-bold mb-4">
                Deaths
            </h3>

          <div class="text-2xl mb-4">
              <span class="font-bold">New: </span>
              {{ stats.NewDeaths}}
          </div>
          <div class="text-2xl mb-4">
              <span class="font-bold">Total: </span>
              {{ stats.TotalDeaths}}
          </div>

        </div>

    </div>
</template>

<script>

export default {
 name: 'DataBoxes',
 props: ['stats']
}
</script>

<style>

</style>