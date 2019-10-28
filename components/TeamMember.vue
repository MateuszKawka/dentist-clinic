<template>
  <figure class="team-member">
    <img src="~/assets/images/doctor.jpg" class="team-member__image">
    <figcaption class="team-member__about">
      <h3 class="team-member__name">{{teamMember.name}}</h3>
      <p class="paragraph">{{teamMember.about}}</p>
    </figcaption>
  </figure>
</template>

<script>
export default {
  name: 'TeamMember',
  props: {
    teamMember: Object
  }
}
</script>