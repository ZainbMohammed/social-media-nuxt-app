<template>
  <div :class="{ 'dark': darkMode }">
    <div class='bg-white dark:bg-dim-900'>
      <div class='min-h-full'>

        <div class='grid grid-cols-12 mx-auto sm:px-6 lg:px-8 lg:max-w-7xl lg:gap-5'>

          <!-- Left Sidebar -->
          <div class='hidden sm:block xs-col-span-1 xl:col-span-2'>
            <div class='sticky top-0'>
              <SidebarLeft />
            </div>
          </div>
          <!-- Main Content -->
          <main class='bg-red-100 col-span-12 md:col-span-8 xl:col-spane-6'>
            <router-view/>
           </main>

          <!-- Right Sidebar -->
          <div class='hidden col-span-12 md:block xl:col-span-4 md:col-span-3 '>
            <div class='sticky top-0'>
              <SidebarRight />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
const darkMode = ref(false)

</script>
