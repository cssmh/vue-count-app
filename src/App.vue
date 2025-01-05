<template>
  <div id="app">
    <header class="header">
      <nav class="navbar">
        <h1 class="logo">Vue App</h1>
        <ul class="nav-links">
          <li>
            <router-link to="/" :class="{ active: $route.name === 'home' }">
              Home
            </router-link>
          </li>
          <li>
            <router-link to="/about" :class="{ active: $route.name === 'about' }">
              About
            </router-link>
          </li>
        </ul>
      </nav>
    </header>
    <main class="main-content">
      <router-view />
    </main>
    <footer class="footer">
      &copy; 2025 Vue App. All rights reserved.
    </footer>
  </div>
</template>
