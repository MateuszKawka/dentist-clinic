<template>
  <section class="section team" id="team">
    <h2 class="section__title">Our team</h2>
    <TeamMember v-for="item in team" :key="item.name" :teamMember="item"/>
  </section>
</template>

<script>
import TeamMember from "@/components/TeamMember";
export default {
  name: "Team",
  components: {
    TeamMember
  },
  data() {
    return {
      team: [
        {
          name: 'John Doe',
          about: 'Lectus bibendum non suspendisse id tristique amet arcu, fusce pellentesque auctor pellentesque et lorem vulputate nec malesuada ac morbi faucibus et sodales metus',
          imgSrc: '~/assets/images/doctor.jpg'
        },
        {
          name: 'Warren Buffett',
          about: 'Lectus bibendum non suspendisse id tristique amet arcu, fusce pellentesque auctor pellentesque et lorem vulputate nec malesuada ac morbi faucibus et sodales metus',
          imgSrc: '~/assets/images/doctor.jpg'
        },
        {
          name: 'Arthur Fleck',
          about: 'Lectus bibendum non suspendisse id tristique amet arcu, fusce pellentesque auctor pellentesque et lorem vulputate nec malesuada ac morbi faucibus et sodales metus',
          imgSrc: '~/assets/images/doctor.jpg'
        },
        {
          name: 'Jesse Lauriston Livermore',
          about: 'Lectus bibendum non suspendisse id tristique amet arcu, fusce pellentesque auctor pellentesque et lorem vulputate nec malesuada ac morbi faucibus et sodales metus',
          imgSrc: '~/assets/images/doctor.jpg'
        }
      ]
    }
  }
};
</script>