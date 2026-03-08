
<!--Miguel De Freitas u23744512-->
<script setup>
const weather = ref(null)
const fact = ref('') 

onMounted(async () => {
  const apiKey = 'f180c81c75e7a189c7f8d717d959afe3'  

  const wRes = await fetch(
    `http://api.weatherstack.com/current?access_key=${apiKey}&query=Pretoria`  
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
      <h2>🌤 Weather in Gauteng</h2>
      <div v-if="weather">  
        <p>{{ weather.temperature }}°C — {{ weather.weather_descriptions[0] }}</p>
        <p>Humidity: {{ weather.humidity }}% · Wind: {{ weather.wind_speed }} km/h</p>
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
