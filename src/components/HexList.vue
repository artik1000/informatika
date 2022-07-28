<template>
    <div>
        <div class="teamSop1">
            <h1>{{match.team1}}</h1>
        </div>
        <div class="teamSop2">
            <h1>{{match.team2}}</h1>
        </div>
        <div class="roundHexMain">
            <div class="area">
                <div class="stad">
                    <p>{{match.stad}}</p>
                </div>
                <div class="day">
                    <h2>{{match.day + ' ' + month}}</h2>
                </div>
                <div class="time">
                    <time>{{match.time}}</time>
                </div>
                <div class="buyticket">
                    <a>
                        <span>Купить билет</span>
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
  name: 'HexList',
  props: {
    match: {
      type: Object,
      requered: true,
    },
      index: {
          type: Number,
          requered: true,
      },
  },
  data () {
      return {
          month: '',
      }
  },
  beforeMount () {
      if (this.match.month === 1) {
          this.month = 'Января'
      }
      if (this.match.month === 2) {
          this.month = 'Февраля'
      }
      if (this.match.month === 3) {
          this.month = 'Марта'
      }
      if (this.match.month === 4) {
          this.month = 'Апреля'
      }
      if (this.match.month === 5) {
          this.month = 'Мая'
      }
      if (this.match.month === 6) {
          this.month = 'Июня'
      }
      if (this.match.month === 7) {
          this.month = 'Июля'
      }
      if (this.match.month === 8) {
          this.month = 'Августа'
      }
      if (this.match.month === 9) {
          this.month = 'Сентября'
      }
      if (this.match.month === 10) {
          this.month = 'Октября'
      }
      if (this.match.month === 11) {
          this.month = 'Ноября'
      }
      if (this.match.month === 12) {
          this.month = 'Декабря'
      }
  }
};
</script>
<style lang="scss">
    .roundHexMain {
        position: inherit;
        background: white;
        margin: auto;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        border-radius: 10px;
        height: 100%;
        width: 51.42%;
    }
    .area {
        position: inherit;
        z-index: 999;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        display: flex;
        flex-direction: column;
        padding-top: 10%;
        padding-bottom: 20%;
    }
    .roundHexMain:before,
    .roundHexMain:after {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        background: inherit;
        border-radius: inherit;
        height: 100%;
        width: 100%;
        z-index:10;
    }
    .roundHexMain:before {
        -webkit-transform: rotate(60deg);
        -moz-transform: rotate(60deg);
        transform: rotate(60deg);
        transition: all 1s 0.5s;
    }
    .roundHexMain:after {
        -webkit-transform: rotate(-60deg);
        -moz-transform: rotate(-60deg);
        transform: rotate(-60deg);
        transition: all 1s 1s;
    }
    .mainhex {
        transition: 2s;
        width: 350px;
        height: 300px;
        position: inherit;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        margin: auto;
        .teamSop1{
            transition: 2s;
            width: 650px;
            height: 150px;
            position: relative;
            right: 630px;
            bottom: 0px;
            h1{
                color: black !important;
                font-size: 2.5rem;
                position: absolute;
                top: 10px;
                right: 0;
                bottom: 0;
                left: 300px;
                z-index: 999;
            }
        }
        .teamSop1::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: white;
            border: 5px solid #fff;
            border-radius: 15px;
            transform: perspective(200px) rotateX(-20deg);
        }

        .teamSop2{
            transition: 2s;
            width: 700px;
            height: 150px;
            position: relative;
            left: 330px;
            top: 0px;
            h1{
                color: black !important;
                font-size: 2.5rem;
                position: absolute;
                top: 30px;
                right: 400px;
                bottom: 0;
                left: 0;
                z-index: 999;
            }
        }
        .teamSop2::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: white;
            border: 5px solid #fff;
            border-radius: 15px;
            transform: perspective(170px) rotateX(15deg);
        }
        .day{
            margin: auto;
        }
        .stad{
            margin: auto;
        }
        .time{
            margin: auto;
        }
        .buyticket{
            margin: auto;
        }
        p{
            transition: 4s;
            color: black;
            font-size: 1.2rem;
            margin: 0 !important;
        }
        h2{
            transition: 4s;
            color: black;
            font-weight: bold;
            font-size: 2.5rem;
            margin: 0 !important;
        }
        time{
            transition: 4s;
            color: black;
            margin: 0 !important;
            font-size: 1.5rem;
        }
        a{
            transition: 4s;
            color: black;
            margin: 0 !important;
            border: 1.5px solid;
            border-radius: 0.5rem;
            padding-left: 30px;
            padding-right: 30px;
            padding-top: 10px;
            padding-bottom: 10px;
        }
        a:hover{
            color: white;
            background-color: #4a5086;
            transition: 0.5s;
        }
    }

    .topbig{
        transition: 2s;
        width: 180px;
        height: 150px;
        position: inherit;
        top: 0;
        right: 0;
        bottom: 35vh;
        left: 35vw;
        margin: auto;
        display: flex;
        .teamSop2{
            transition: 4s;
            position: inherit;
            left: 1200px;
            h1{
                opacity: 0;
            }
        }
        .teamSop1{
            transition: 4s;
            right: 1600px;
            h1{
                opacity: 0;
            }
        }
        h2{
            font-size: 1.2rem;
            color: black;
        }
        .day{
            margin: auto;
        }
        p{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        time{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        a{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        .stad{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        .time{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        .buyticket{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
    }
    .topsmall{
        transition: 2s;
        color: black;
        width: 140px;
        height: 112.5px;
        position: inherit;
        top: 0;
        right: 0;
        bottom: 55vh;
        left: 55vw;
        margin: auto;
        display: flex;
        .teamSop2{
            transition: 2s;
            position: relative;
            left: 1200px;
            h1{
                opacity: 0;
            }
        }
        .teamSop1{
            transition: 2s;
            position: relative;
            right: 1600px;
            h1{
                opacity: 0;
            }
        }
        h2{
            font-size: 1rem;
            color: black;
        }
        .day{
            margin: auto;
        }
        p{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        time{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        a{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        .stad{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        .time{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        .buyticket{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
    }
    .bottombig{
        transition: 2s;
        width: 180px;
        height: 150px;
        position: inherit;
        top: 35vh;
        right: 35vw;
        bottom: 0;
        left: 0;
        margin: auto;
        display: flex;
        .teamSop2{
            transition: 2s;
            position: relative;
            left: 1200px;
            h1{
                opacity: 0;
            }
        }
        .teamSop1{
            transition: 2s;
            position: relative;
            right: 1600px;
            h1{
                opacity: 0;
            }
        }
        h2{
            font-size: 1.2rem;
            color: black;
        }
        .day{
            margin: auto;
        }
        p{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        time{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        a{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        .stad{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        .time{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        .buyticket{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
    }
    .bottomsmall{
        transition: 2s;
        color: black;
        width: 140px;
        height: 112.5px;
        position: inherit;
        bottom: 0;
        left: 0;
        top: 55vh;
        right: 55vw;
        margin: auto;
        display: flex;
        .teamSop2{
            transition: 2s;
            position: relative;
            left: 1200px;
            h1{
                opacity: 0;
            }
        }
        .teamSop1{
            transition: 2s;
            position: relative;
            right: 1600px;
            h1{
                opacity: 0;
            }
        }
        h2{
            font-size: 1rem;
            color: black;
        }
        .day{
            margin: auto;
        }
        p{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        time{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        a{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        .stad{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        .time{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
        .buyticket{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
    }
    .close{
        width: 0px;
        height: 0px;
        opacity: 0;
    }
    @media screen and (min-device-width: 280px) and (max-device-width: 319px) {
        .mainhex {
            transition: 2s;
            width: 180px;
            height: 150px;
            position: inherit;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            margin: auto;
            .teamSop1{
                transition: 2s;
                width: 90px;
                height: 70px;
                position: relative;
                right: 80px;
                bottom: 0px;
                h1{
                    color: black !important;
                    font-size: 0.9rem;
                    position: absolute;
                    top: 0px;
                    right: 0;
                    bottom: 0;
                    left: 20px;
                    z-index: 999;
                }
            }
            .teamSop1::before {
                content: "";
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                background: white;
                border: 5px solid #fff;
                border-radius: 10px;
                transform: perspective(48px) rotateX(-30deg);
            }

            .teamSop2{
                transition: 2s;
                width: 90px;
                height: 80px;
                position: relative;
                left: 170px;
                top: 0px;
                h1{
                    color: black !important;
                    font-size: 0.9rem;
                    position: absolute;
                    top: 30px;
                    right: 30px;
                    bottom: 0;
                    left: 0;
                    z-index: 999;
                }
            }
            .teamSop2::before {
                content: "";
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                background: white;
                border: 5px solid #fff;
                border-radius: 10px;
                transform: perspective(90px) rotateX(45deg);
            }
            .day{
                margin: auto;
            }
            .stad{
                margin: auto;
            }
            .time{
                margin: auto;
            }
            .buyticket{
                margin: auto;
            }
            p{
                transition: 4s;
                color: black;
                font-size: 1rem;
                margin: 0 !important;
            }
            h2{
                transition: 4s;
                color: black;
                font-weight: bold;
                font-size: 1.5rem;
                margin: 0 !important;
            }
            time{
                transition: 4s;
                color: black;
                margin: 0 !important;
                font-size: 1rem;
            }
            a{
                font-size: 0.5rem;
                transition: 4s;
                color: black;
                margin: 0 !important;
                border: 0.5px solid;
                border-radius: 0.3rem;
                padding-left: 10px;
                padding-right: 10px;
                padding-top: 5px;
                padding-bottom: 5px;
            }
            a:hover{
                color: white;
                background-color: #4a5086;
                transition: 0.5s;
            }
        }
        .topbig{
            transition: 2s;
            width: 140px;
            height: 112.5px;
            position: inherit;
            top: 0;
            right: 0;
            bottom: 42vh;
            left: 42vw;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 4s;
                position: inherit;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 4s;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 1.2rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
        .topsmall{
            transition: 2s;
            color: black;
            width: 112px;
            height: 90px;
            position: inherit;
            top: 0;
            right: 0;
            bottom: 70vh;
            left: 70vw;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 2s;
                position: relative;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 2s;
                position: relative;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 0.8rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
        .bottombig{
            transition: 2s;
            width: 140px;
            height: 112.5px;
            position: inherit;
            top: 42vh;
            right: 42vw;
            bottom: 0;
            left: 0;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 2s;
                position: relative;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 2s;
                position: relative;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 1.2rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
        .bottomsmall{
            transition: 2s;
            color: black;
            width: 112px;
            height: 90px;
            position: inherit;
            bottom: 0;
            left: 0;
            top: 80vh;
            right: 80vw;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 2s;
                position: relative;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 2s;
                position: relative;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 0.8rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
    }
    @media screen and (min-device-width: 320px) and (max-device-width: 479px) {
        .mainhex {
            transition: 2s;
            width: 180px;
            height: 150px;
            position: inherit;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            margin: auto;
            .teamSop1{
                transition: 2s;
                width: 150px;
                height: 70px;
                position: relative;
                right: 140px;
                bottom: 0px;
                h1{
                    color: black !important;
                    font-size: 0.9rem;
                    position: absolute;
                    top: 10px;
                    right: 0;
                    bottom: 0;
                    left: 20px;
                    z-index: 999;
                }
            }
            .teamSop1::before {
                content: "";
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                background: white;
                border: 5px solid #fff;
                border-radius: 10px;
                transform: perspective(48px) rotateX(-20deg);
            }

            .teamSop2{
                transition: 2s;
                width: 150px;
                height: 80px;
                position: relative;
                left: 170px;
                top: 0px;
                h1{
                    color: black !important;
                    font-size: 0.9rem;
                    position: absolute;
                    top: 30px;
                    right: 30px;
                    bottom: 0;
                    left: 0;
                    z-index: 999;
                }
            }
            .teamSop2::before {
                content: "";
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                background: white;
                border: 5px solid #fff;
                border-radius: 10px;
                transform: perspective(90px) rotateX(35deg);
            }
            .day{
                margin: auto;
            }
            .stad{
                margin: auto;
            }
            .time{
                margin: auto;
            }
            .buyticket{
                margin: auto;
            }
            p{
                transition: 4s;
                color: black;
                font-size: 0.8rem;
                margin: 0 !important;
            }
            h2{
                transition: 4s;
                color: black;
                font-weight: bold;
                font-size: 1.2rem;
                margin: 0 !important;
            }
            time{
                transition: 4s;
                color: black;
                margin: 0 !important;
                font-size: 1rem;
            }
            a{
                font-size: 0.5rem;
                transition: 4s;
                color: black;
                margin: 0 !important;
                border: 0.5px solid;
                border-radius: 0.3rem;
                padding-left: 10px;
                padding-right: 10px;
                padding-top: 5px;
                padding-bottom: 5px;
            }
            a:hover{
                color: white;
                background-color: #4a5086;
                transition: 0.5s;
            }
        }
        .topbig{
            transition: 2s;
            width: 140px;
            height: 112.5px;
            position: inherit;
            top: 0;
            right: 0;
            bottom: 40vh;
            left: 40vw;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 4s;
                position: inherit;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 4s;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 1rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
        .topsmall{
            transition: 2s;
            color: black;
            width: 112px;
            height: 90px;
            position: inherit;
            top: 0;
            right: 0;
            bottom: 70vh;
            left: 70vw;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 2s;
                position: relative;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 2s;
                position: relative;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 0.8rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
        .bottombig{
            transition: 2s;
            width: 140px;
            height: 112.5px;
            position: inherit;
            top: 40vh;
            right: 40vw;
            bottom: 0;
            left: 0;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 2s;
                position: relative;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 2s;
                position: relative;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 1rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
        .bottomsmall{
            transition: 2s;
            color: black;
            width: 112px;
            height: 90px;
            position: inherit;
            bottom: 0;
            left: 0;
            top: 75vh;
            right: 75vw;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 2s;
                position: relative;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 2s;
                position: relative;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 0.8rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
    }
    @media screen and (min-device-width: 768px) and (max-device-width: 1023px) {
        .mainhex {
            transition: 2s;
            width: 350px;
            height: 300px;
            position: inherit;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            margin: auto;
            .teamSop1{
                transition: 2s;
                width: 600px;
                height: 150px;
                position: relative;
                right: 580px;
                bottom: 0px;
                h1{
                    color: black !important;
                    font-size: 2rem;
                    position: absolute;
                    top: 20px;
                    right: 0px;
                    bottom: 0;
                    left: 400px;
                    z-index: 999;
                }
            }
            .teamSop1::before {
                content: "";
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                background: white;
                border: 5px solid #fff;
                border-radius: 15px;
                transform: perspective(180px) rotateX(-20deg);
            }

            .teamSop2{
                transition: 2s;
                width: 700px;
                height: 150px;
                position: relative;
                left: 330px;
                top: 0px;
                h1{
                    color: black !important;
                    font-size: 2rem;
                    position: absolute;
                    top: 40px;
                    right: 480px;
                    bottom: 0;
                    left: 0;
                    z-index: 999;
                }
            }
            .teamSop2::before {
                content: "";
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                background: white;
                border: 5px solid #fff;
                border-radius: 15px;
                transform: perspective(180px) rotateX(15deg);
            }
            .day{
                margin: auto;
            }
            .stad{
                margin: auto;
            }
            .time{
                margin: auto;
            }
            .buyticket{
                margin: auto;
            }
            p{
                transition: 4s;
                color: black;
                font-size: 1.2rem;
                margin: 0 !important;
            }
            h2{
                transition: 4s;
                color: black;
                font-weight: bold;
                font-size: 2.5rem;
                margin: 0 !important;
            }
            time{
                transition: 4s;
                color: black;
                margin: 0 !important;
                font-size: 1.5rem;
            }
            a{
                transition: 4s;
                color: black;
                margin: 0 !important;
                border: 1.5px solid;
                border-radius: 0.5rem;
                padding-left: 30px;
                padding-right: 30px;
                padding-top: 10px;
                padding-bottom: 10px;
            }
            a:hover{
                color: white;
                background-color: #4a5086;
                transition: 0.5s;
            }
        }

        .topbig{
            transition: 2s;
            width: 180px;
            height: 150px;
            position: inherit;
            top: 0;
            right: 0;
            bottom: 40vh;
            left: 40vw;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 4s;
                position: inherit;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 4s;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 1.2rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
        .topsmall{
            transition: 2s;
            color: black;
            width: 140px;
            height: 112.5px;
            position: inherit;
            top: 0;
            right: 0;
            bottom: 62vh;
            left: 62vw;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 2s;
                position: relative;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 2s;
                position: relative;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 1rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
        .bottombig{
            transition: 2s;
            width: 180px;
            height: 150px;
            position: inherit;
            top: 40vh;
            right: 40vw;
            bottom: 0;
            left: 0;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 2s;
                position: relative;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 2s;
                position: relative;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 1.2rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
        .bottomsmall{
            transition: 2s;
            color: black;
            width: 140px;
            height: 112.5px;
            position: inherit;
            bottom: 0;
            left: 0;
            top: 62vh;
            right: 62vw;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 2s;
                position: relative;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 2s;
                position: relative;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 1rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
        .close{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
    }
    @media screen and (min-device-width: 480px) and (max-device-width: 767px) {
        .mainhex {
            transition: 2s;
            width: 180px;
            height: 150px;
            position: inherit;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            margin: auto;
            .teamSop1{
                transition: 2s;
                width: 210px;
                height: 70px;
                position: relative;
                right: 210px;
                bottom: 0px;
                h1{
                    color: black !important;
                    font-size: 1.5rem;
                    position: absolute;
                    top: 0px;
                    right: 0;
                    bottom: 0;
                    left: 20px;
                    z-index: 999;
                }
            }
            .teamSop1::before {
                content: "";
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                background: white;
                border: 5px solid #fff;
                border-radius: 10px;
                transform: perspective(60px) rotateX(-20deg);
            }

            .teamSop2{
                transition: 2s;
                width: 210px;
                height: 80px;
                position: relative;
                left: 180px;
                top: 0px;
                h1{
                    color: black !important;
                    font-size: 1.5rem;
                    position: absolute;
                    top: 15px;
                    right: 30px;
                    bottom: 0;
                    left: 0;
                    z-index: 999;
                }
            }
            .teamSop2::before {
                content: "";
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                background: white;
                border: 5px solid #fff;
                border-radius: 10px;
                transform: perspective(90px) rotateX(25deg);
            }
            .day{
                margin: auto;
            }
            .stad{
                margin: auto;
            }
            .time{
                margin: auto;
            }
            .buyticket{
                margin: auto;
            }
            p{
                transition: 4s;
                color: black;
                font-size: 1rem;
                margin: 0 !important;
            }
            h2{
                transition: 4s;
                color: black;
                font-weight: bold;
                font-size: 1.5rem;
                margin: 0 !important;
            }
            time{
                transition: 4s;
                color: black;
                margin: 0 !important;
                font-size: 1rem;
            }
            a{
                font-size: 0.5rem;
                transition: 4s;
                color: black;
                margin: 0 !important;
                border: 0.5px solid;
                border-radius: 0.3rem;
                padding-left: 10px;
                padding-right: 10px;
                padding-top: 5px;
                padding-bottom: 5px;
            }
            a:hover{
                color: white;
                background-color: #4a5086;
                transition: 0.5s;
            }
        }
        .topbig{
            transition: 2s;
            width: 140px;
            height: 112.5px;
            position: inherit;
            top: 0;
            right: 0;
            bottom: 35vh;
            left: 35vw;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 4s;
                position: inherit;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 4s;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 1.2rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
        .topsmall{
            transition: 2s;
            color: black;
            width: 112px;
            height: 90px;
            position: inherit;
            top: 0;
            right: 0;
            bottom: 60vh;
            left: 60vw;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 2s;
                position: relative;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 2s;
                position: relative;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 0.8rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
        .bottombig{
            transition: 2s;
            width: 140px;
            height: 112.5px;
            position: inherit;
            top: 35vh;
            right: 35vw;
            bottom: 0;
            left: 0;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 2s;
                position: relative;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 2s;
                position: relative;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 1.2rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
        .bottomsmall{
            transition: 2s;
            color: black;
            width: 112px;
            height: 90px;
            position: inherit;
            bottom: 0;
            left: 0;
            top: 65vh;
            right: 65vw;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 2s;
                position: relative;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 2s;
                position: relative;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 0.8rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
    }
@media screen and (min-device-width: 1024px) and (max-device-width: 1279px) {
        .roundHexMain {
            position: inherit;
            background: white;
            margin: auto;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            border-radius: 10px;
            height: 100%;
            width: 51.42%;
        }
        .area {
            position: inherit;
            z-index: 999;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            display: flex;
            flex-direction: column;
            padding-top: 10%;
            padding-bottom: 20%;
        }
        .roundHexMain:before,
        .roundHexMain:after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            background: inherit;
            border-radius: inherit;
            height: 100%;
            width: 100%;
            z-index:10;
        }
        .roundHexMain:before {
            -webkit-transform: rotate(60deg);
            -moz-transform: rotate(60deg);
            transform: rotate(60deg);
            transition: all 1s 0.5s;
        }
        .roundHexMain:after {
            -webkit-transform: rotate(-60deg);
            -moz-transform: rotate(-60deg);
            transform: rotate(-60deg);
            transition: all 1s 1s;
        }
        .mainhex {
            transition: 2s;
            width: 300px;
            height: 260px;
            position: inherit;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            margin: auto;
            .teamSop1{
                transition: 2s;
                width: 600px;
                height: 130px;
                position: relative;
                right: 580px;
                bottom: 0px;
                h1{
                    color: black !important;
                    font-size: 2.5rem;
                    position: absolute;
                    top: 0;
                    right: 0;
                    bottom: 0;
                    left: 300px;
                    margin-top: 40px;
                    z-index: 999;
                }
            }
            .teamSop1::before {
                content: "";
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                background: white;
                border: 5px solid #fff;
                border-radius: 15px;
                transform: perspective(200px) rotateX(-22deg);
            }

            .teamSop2{
                transition: 2s;
                width: 700px;
                height: 130px;
                position: relative;
                left: 280px;
                top: 0px;
                h1{
                    color: black !important;
                    font-size: 2.5rem;
                    position: absolute;
                    top: 0px;
                    right: 300px;
                    bottom: 0;
                    left: 0;
                    z-index: 999;
                }
            }
            .teamSop2::before {
                content: "";
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                background: white;
                border: 5px solid #fff;
                border-radius: 15px;
                transform: perspective(200px) rotateX(18deg);
            }
            .day{
                margin: auto;
            }
            .stad{
                margin: auto;
            }
            .time{
                margin: auto;
            }
            .buyticket{
                margin: auto;
            }
            p{
                transition: 4s;
                color: black;
                font-size: 1.2rem;
                margin: 0 !important;
            }
            h2{
                transition: 4s;
                color: black;
                font-weight: bold;
                font-size: 2.5rem;
                margin: 0 !important;
            }
            time{
                transition: 4s;
                color: black;
                margin: 0 !important;
                font-size: 1rem;
            }
            a{
                transition: 4s;
                color: black;
                margin: 0 !important;
                border: 1.5px solid;
                border-radius: 0.5rem;
                padding-left: 15px;
                padding-right: 15px;
                padding-top: 5px;
                padding-bottom: 5px;
            }
            a:hover{
                color: white;
                background-color: #4a5086;
                transition: 0.5s;
            }
        }

        .topbig{
            transition: 2s;
            width: 140px;
            height: 112.5px;
            position: inherit;
            top: 0;
            right: 0;
            bottom: 35vh;
            left: 35vw;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 4s;
                position: inherit;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 4s;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 1.2rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
        .topsmall{
            transition: 2s;
            color: black;
            width: 112px;
            height: 90px;
            position: inherit;
            top: 0;
            right: 0;
            bottom: 55vh;
            left: 55vw;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 2s;
                position: relative;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 2s;
                position: relative;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 0.8rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
        .bottombig{
            transition: 2s;
            width: 140px;
            height: 112.5px;
            position: inherit;
            top: 35vh;
            right: 35vw;
            bottom: 0;
            left: 0;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 2s;
                position: relative;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 2s;
                position: relative;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 1.2rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
        .bottomsmall{
            transition: 2s;
            color: black;
            width: 112px;
            height: 90px;
            position: inherit;
            bottom: 0;
            left: 0;
            top: 55vh;
            right: 55vw;
            margin: auto;
            display: flex;
            .teamSop2{
                transition: 2s;
                position: relative;
                left: 1200px;
                h1{
                    opacity: 0;
                }
            }
            .teamSop1{
                transition: 2s;
                position: relative;
                right: 1600px;
                h1{
                    opacity: 0;
                }
            }
            h2{
                font-size: 0.8rem;
                color: black;
            }
            .day{
                margin: auto;
            }
            p{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            a{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .stad{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .time{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
            .buyticket{
                width: 0px;
                height: 0px;
                opacity: 0;
            }
        }
        .close{
            width: 0px;
            height: 0px;
            opacity: 0;
        }
    }
</style>
