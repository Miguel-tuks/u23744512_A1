
<!--Miguel De Freitas u23744512-->
<script setup>
const weather = ref(null)
const fact = ref('') 

onMounted(async () => {
  const wRes = await fetch(
  'https://api.open-meteo.com/v1/forecast?latitude=-25.74&longitude=28.22&current=temperature_2m,relative_humidity_2m,wind_speed_10m,weather_code'
)
const wData = await wRes.json()
weather.value = wData.current
  const fRes = await fetch('https://uselessfacts.jsph.pl/api/v2/facts/random?language=en')
  const fData = await fRes.json()
  fact.value = fData.text
})
</script>

<template>
  <div>
    <section>
      <h1>Hi I am Miguel De Freitas</h1>
      <img src="/photo.jpg" alt="My photo" width = "150"/>
      <p>I am a student at the University of Pretoria studying Information and Knowledge Systems</p>
    </section>

   <section>
  <h2>Weather in Gauteng</h2>
  <div v-if="weather">
    <p>{{ weather.temperature_2m }}°C</p>
    <p>Humidity: {{ weather.relative_humidity_2m }}% · Wind: {{ weather.wind_speed_10m }} km/h</p>
  </div>
  <p v-else>Loading weather…</p>
</section>

    <section>
      <h2>💡 Random Fact</h2>
      <p v-if="fact">{{ fact }}</p>
      <p v-else>Loading fact…</p>
    </section>
  </div>
</template>
