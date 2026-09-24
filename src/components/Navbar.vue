<template>
 <nav>
 <h2>Azzahrascraf_ Onlineshop</h2>
 <RouterLink to="/">Landing</RouterLink> |
 <RouterLink to="/product">Product</RouterLink> |
 <RouterLink to="/about">About</RouterLink> |
 <router-link to="/contact">Contact</router-link>
 </nav>
 <hr />
</template>
<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  background-color: rgb(217, 164, 223);
}
</style>
<style scoped>
nav{
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: nowrap;
  padding: 20px 50px;
  
}
</style>