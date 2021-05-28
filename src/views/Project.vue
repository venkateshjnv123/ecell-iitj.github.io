<template lang="pug">
div(align='center', justify='center')
  div(v-if="loading")
        Preloader
  div(v-else)
    v-container
      v-row(justify='left')
        v-flex.mb-6(v-for='Project in projects', :key='Project.name', xs12='',sm12='', md6='',lg4='',xl4='')
          ProjectCard(:Project='Project')
</template>
<script>
const ProjectCard = () => import("../components/ProjectCard");
const Preloader = () => import("../components/Preloader");
export default {
  name: "Project",
  components: { ProjectCard, Preloader },
  data: () => ({
    loading: true,
    projects: []
  }),
  methods: {
    fetchProjects() {
      this.loading = true;
      fetch(
        "https://spreadsheets.google.com/feeds/list/1PJoBY085s4N6MNqQ3t0utZtwL8k8EtCMN1VVrwa8nBU/omtjtxx/public/values?alt=json"
      )
        .then(e =>
          e.json().then(e => {
            this.projects = [...e.feed.entry];
          })
        )
        .finally(() => (this.loading = false));
    }
  },
  mounted() {
    this.fetchProjects();
  }
};
</script>
