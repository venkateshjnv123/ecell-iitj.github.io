<template lang="pug">
div#inspire
  v-content.pa-0(style="height:auto; width:100%")
    v-container.mt-12.mt-sm-0.pt-sm-0(style='z-index:1 ; height:auto;')
      v-row.mt-sm-0.pt-sm-3.px-4(align='center' justify='center' style='height:100%')
        v-col.text-left.px-md-3(sm='12' cols='12' :style="[$vuetify.breakpoint.mdAndUp ? 'margin-top:50pt' : 'margin-top:35pt']")
          .pl-md-10.pr-sm-7(style='width:100%;')
            h1.font-weight-bold.mb-1.mb-sm-5(:class="[$vuetify.breakpoint.lgAndUp ? 'h2' :'h4']") About Us
            h2.font-weight-regular(:class="[$vuetify.breakpoint.lgAndUp ? 'h3' : 'subtitle-1']")
              span.blue--text Entrepreneurship-Cell IIT Jodhpur
              |  is a student body that focuses on developing and promoting entrepreneurial eco-system and start-up skills in creative and potential minds. It focuses on various dimensions of the corporate world that revolves around an entrepreneur. Being a student-run body, we educate people about different aspects of a business, guide and promote entrepreneurial ideas and provide resources to help them establish, nurture and run their own startup.
        v-btn.outlined.ma-2--text Read More
</template>
<script>
export default {};
</script>
