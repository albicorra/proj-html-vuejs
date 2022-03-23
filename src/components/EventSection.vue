<template>
  <div class="container-small section-wrapper">
    <h4 class="subtitle">Wanna transform your life?</h4>
    <h1 class="big-title">Upcoming Events</h1>

    <div class="event-container">
      
      <div class="event-wrapper">
        <div class="event-place">
          <p><i class="fa-solid fa-location-dot"></i>  Texas, US</p>
          <div>Storytelling Workshop</div>
        </div>

        <div class="event-date">
          <div>22</div>
          <div>apr</div>
          <button>get ticket</button>
        </div>
      </div>

      <div></div>
    
    </div>
  </div>
</template>

<script>
export default {
  name: 'EventSection',
  
}
</script>

<style scoped lang="scss">
  .section-wrapper{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    padding: 110px 0px 200px 0px;

    .event-container{
      display: flex;
      align-items: center;
      flex-wrap: wrap;
      gap: 30px;

      .event-wrapper{
        width: 48%;
        background-color: #F8F8F8;
        padding: 20px;
        border-radius: 5px;
        display: flex;
      }
    }
  }
</style>
