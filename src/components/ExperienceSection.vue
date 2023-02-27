<template>
    <h2 class="py-3 px-5">Experiences</h2>
    <div class="py-2" v-for = "(e,index) in experiences" :key="e">
      <div class="row justify-content-start">
        <div class="col-1 text-end pt-1">
          <div class="dot"></div>
          <br>
          <div class="vl" v-if="index < experiences.length - 1"></div>
        </div>
        <div class="col-11">
          <p class="title">{{ e.company }}</p>
          <p class="duration">{{ e.duration }}</p>
          <p class="w-400">{{ e.title.fr }}</p>
          <p>Réalisation:</p>
          <ul>
            <li class="px-2" v-for="c in e.content.fr" :key="c">
              <span v-if="subContentList(c).length == 1">{{ c }}</span>
              <ul class="sub-content-list" v-else>
                <li v-for="i in subContentList(c)" :key="i">
                  {{ i }}
                </li>
              </ul>
            </li>
          </ul>
          <p v-if="e.environment != null">Environnement technique / Méthodologie: {{ e.environment }}</p>
        </div>
      </div>
    </div>
    
</template>

<script>
import profile from '../json/profile.json'
export default{
  data () {
    return {
      experiences : profile.experiences
    }
  },
  methods: {
    subContentList(content) {
      let l = content.split('|');
      console.log(l);
      return l;
      
    }
  }
}
</script>

<style>
.title{
  font-weight: 500;
  font-size: 23px;
}

.w-400{
  font-weight: 500;
}

.duration{
  font-style: italic;
}

.sub-content-list{
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.dot {
  height: 25px;
  width: 25px;
  background: radial-gradient(ellipse at top, #C9D7F3, transparent);
  border-radius: 50%;
  display: inline-block;
}

.vl {
  border-left: 1px solid #A9A9A9;
  height: 95%;
  float: right;
  margin-right: 12.5px;
}
</style>