<template>
  <div :class="{ 'dark': darkMode }">
    <div class='bg-white dark:bg-dim-900'>
      <div class='min-h-full'>

        <div class='grid grid-col-12 mx-auto sm:px-6 lg:px-8 lg:max-w-7xl lg:gap-5'>

          <!-- Left Sidebar -->
          <div class='md:block xs-col-span-1 xl:col-span-2'>
            <div class='sticky top-0'>

              <SidebarLeft />
              <!-- <sidebar-left />  => It can be like this -->

            </div>
          </div>
          <!-- Main Content -->
          <!-- Right Sidebar -->
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
const darkMode = ref(false)

</script>
