<template>
  <div id="app">
    <AppHeader />
    <AppHome />
  </div>
</template>

<script>
import './styles/global.css';
import AppHeader from './components/Header';
import AppHome from './pages/Home'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppHome
  }
}
</script>
