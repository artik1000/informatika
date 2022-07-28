<template>
  <div class="home">
    <HexList
            v-for="(match, index) in matches.slice(beforeDate,afterDate)"
            :key="match.id"
            :match="match"
            :index="index"
            :class="classes[index]"
            v-show="match.id > -1"
            @click="changeMethod(match)"
            @wheel.prevent="handleWheel($event)"
    />
    </div>
</template>

<script>
import HexList from '@/components/HexList'
export default {
  name: 'HomeView',
  components: {
    HexList,
  },
  data() {
    return {
      matches: [
        {id: 0, day: 22, month: 10, stad: 'Стадион', time: '13:00', team1: 'Спартак', team2: 'Зенит'},
        {id: 1, day: 12, month: 9, stad: 'Стадион', time: '13:00', team1: 'Спартак', team2: 'Зенит'},
        {id: 2, day: 22, month: 7, stad: 'Стадион', time: '16:00', team1: 'Рубин', team2: 'Зенит'},
        {id: 3, day: 30, month: 7, stad: 'Стадион', time: '16:00', team1: 'Рубин', team2: 'Зенит'},
        {id: 4, day: 31, month: 7, stad: 'Стадион', time: '16:00', team1: 'Зенит', team2: 'Спартак'},
        {id: 5, day: 12, month: 7, stad: 'Стадион', time: '19:00', team1: 'Ростов', team2: 'Рубин'},
        {id: 6, day: 10, month: 6, stad: 'Стадион', time: '12:00', team1: 'Интер', team2: 'Ювентус'},
        {id: 7, day: 5, month: 5, stad: 'Стадион', time: '18:00', team1: 'Челси', team2: 'Ман.Сити'},
        {id: 8, day: 4, month: 4, stad: 'Стадион', time: '18:00', team1: 'Челси', team2: 'Ман.Сити'},
      ],
      classes: [
        'bottomsmall',
        'bottombig',
        'mainhex',
        'topbig',
        'topsmall'
      ],
      curentDate: 0,
      beforeDate: 0,
      afterDate: 0,
    }
  },
  beforeMount () {
      this.matches.splice(0,0,{},{})
      let date = new Date();
      let nearEvaent = [...this.matches].filter((e) => e.month === date.getMonth() + 1).filter((e) => e.day >= date.getDate())[0]
      this.curentDate = this.matches.indexOf(nearEvaent)
      this.beforeDate = this.curentDate - 2
      this.afterDate = this.curentDate + 3
  },
  methods: {
    changeMethod(match) {
        this.curentDate = this.matches.indexOf(match)
        this.beforeDate = this.curentDate - 2
        this.afterDate = this.curentDate + 3
    },

    handleWheel(event) {
      if (event.deltaY < 0 && this.afterDate < this.matches.length + 2) {
         this.beforeDate = this.beforeDate + 1
         this.afterDate = this.afterDate + 1
      } else if (event.deltaY > 0 && this.beforeDate > 0){
          this.beforeDate = this.beforeDate - 1
          this.afterDate = this.afterDate - 1
      }
    }
  },
};
</script>
<style lang="scss">
  .home{
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    margin: auto;
    height: 80vh;
    width: 80vw;
  }
</style>
