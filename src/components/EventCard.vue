<template>
  <div class="event-wrapper">
        <div class="event-place">
          <p><i class="fa-solid fa-location-dot"></i>  {{city}}</p>
          <div>{{activity}}</div>
        </div>

        <div class="event-date">
          <div class="date">{{date}}</div>
          <div class="month">{{month}}</div>
          <button class="green-button ticket">Get ticket</button>
        </div>
    </div>
</template>

<script>
export default {
  name: 'EventCard',
  props: {
    city: String,
    activity: String,
    date: String,
    month: String
  }
}
</script>

<style scoped lang="scss">
    .event-wrapper{
        width: 48%;
        background-color: #F8F8F8;
        padding: 30px;
        border-radius: 5px;
        display: flex;
        cursor: pointer;
        transition: 100ms;

        .event-place{
            width: 80%;

            p{
                color: #7e7e7e;
                font-size: 14px;
                margin-bottom: 10px;
            }

            div{
                font-size: 20px;
                font-weight: 700;
            }
        }

        .event-date{
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 20%;

            .date{
                font-size: 48px;
                color: #20ad96;
            }

            .month{
                font-size: 15px;
                font-weight: 700;
                text-transform: uppercase;
            }

            .green-button.ticket{
                padding: 10px;
                width: 100%;
                margin-top: 10px ;
            }
        }
    }

    .event-wrapper:hover{
        background-color: #fff;
        box-shadow: 0px 0px 10px rgba(0,0,0, 0.3);
        border-left: 3px solid #20ad96;
    }

    .event-wrapper:hover .green-button.ticket{
        background-color: #3F3A64;
        color: #fff;
    }


</style>
