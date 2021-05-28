<template lang="pug">
v-row(justify='left')
  v-col
    v-card.elevation-5(:width="getProfileWidth" :height='getheight' v-on:mouseover='myfunction' v-on:mouseleave='myfunction2')
      v-card.px-3(:width="getProfileWidth" flat :height='getheight')
        v-row 
          v-col(cols="12" style="background-color:#fff") 
            v-avatar(:size="(11/15)*getProfileWidth")
                img(:src="Profile.gsx$src.$t" contain )
                  
                      
          v-col.pa-2(cols="12")  
            div
              h4.mt-1.mb-n2 {{ Profile.gsx$name.$t }}
              v-row.justify-center
                v-col
                  h6 {{ Profile.gsx$currentdesignation.$t }} | {{Profile.gsx$ecelldesignation.$t }}
                        
      v-expand-transition
        v-card(:height="getheight" v-if='active' class="transition-fast-in-fast-out v-card--reveal" :width="getProfileWidth" justify-content='center')
          v-row(align='center' justify='center')
          div()
            v-col.pa-2(cols="12" align-items='center')  
              h4.mt-1.mb-n2 {{ Profile.gsx$name.$t }}
              v-row.justify-center
                v-col
                  h6 {{ Profile.gsx$currentdesignation.$t }} | {{Profile.gsx$ecelldesignation.$t }}
            v-row.justify-center.align-center
              v-col(cols="12")  {{ Profile.gsx$info.$t }}
            v-row.justify-center.align-center
              v-btn(color='red',:href="Profile.gsx$linkemail.$t",target='_blank',v-if='Profile.gsx$linkemail.$t' icon small)
                v-icon(color='red') mdi-email
              v-btn(color='black',:href="Profile.gsx$linkgithub.$t",target='_blank',v-if='Profile.gsx$linkgithub.$t' icon small)
                v-icon(color='black') mdi-github
              v-btn(color='orange',:href="Profile.gsx$linkgitlab.$t",target='_blank',v-if='Profile.gsx$linkgitlab.$t' icon small)
                v-icon(color='orange') mdi-gitlab
              v-btn(color='blue',:href="Profile.gsx$linklinkedin.$t",target='_blank',v-if='Profile.gsx$linklinkedin.$t' icon small)
                v-icon(color='blue') mdi-linkedin     

              
</template>
<script>
export default {
  name: "ProfileCard",
  props: ["Profile"],
  data: () => ({
    pageNo: 1,
    active: false,
    getProfileWidth: "230",
    getheight: "280"
  }),
  methods: {
    myfunction: function() {
      this.active = true;
    },
    myfunction2: function() {
      this.active = false;
    }
  }
};
</script>
<style scoped>
.v-card--reveal {
  bottom: 0;
  opacity: 1 !important;
  position: absolute;
  width: 100%;
}
</style>
