<template>
  <div class="text-center lg:text-left m-10 justify-center">
  <h1 class="font-extrabold title text-transparent text-5xl lg:text-8xl bg-clip-text bg-gradient-to-r from-pink-500 via-red-500 to-yellow-500">Frequently Asked Questions </h1>
    <div class="text-center lg:text-left m-10">
      <div v-for="item in items" v-bind:key="item.id">
        <p class="mb-3 text-2xl font-semibold">{{item.question}}</p>
        <p class="mb-3 font-thin pb-6">
          {{item.answer}}
        </p>
      </div>
      <h1 class='text-2xl'>Have any more questions? <NuxtLink to='/Contact' class='text-sky-600'>Contact us.</NuxtLink></h1>
    </div>
  </div>
 

      
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          id: 1,
          question: "What is Club.dev?",
          answer: "Club.dev is a society founded by a group of students with a strong passion for computer science."
        },
        {
          id: 2,
          question: "What is the purpose of Club.dev?",
          answer: "This society focuses on development of projects as well as real world skills required that can be marketed easily to help prepare for the future."
        },
        {
          id: 3,
          question: "What level of programming should I have to join?",
          answer: "Intermediate experience in written program languages, or any Computer Science students from IGCSE or IB."
        },
        {
          id: 4,
          question: "When and where will the Club be hosted",
          answer: "It will be hosted every tuesday lunchtime @ ICT3. External sessions may considered later on.",
        },
        {
          id: 5,
          question: "What skills will be taught?",
          answer: "Although it is not neccessary to participate in the sessions, we will cover usage of tools and skills used in real world development like version control with git. ",
        },
      ]
    }
  },
  head() {
    return {
      title: 'club.dev | FAQ'
    }
  }
}
</script>
