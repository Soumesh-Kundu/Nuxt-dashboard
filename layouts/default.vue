<template>
  <div>
    <div>
      <Sidebar />
      <div class="sm:pl-64">
        <slot />
      </div>
    </div>
  </div>
</template>

<style>
body{
  @apply bg-gray-100
}
::-webkit-scrollbar{
  width:8px;
}
::-webkit-scrollbar-track{
  border-radius: 999px;
  @apply bg-gray-50;
}
::-webkit-scrollbar-thumb{
  @apply bg-gray-400 rounded-full
}
</style>