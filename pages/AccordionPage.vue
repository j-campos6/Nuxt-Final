<template>
      <!-- Main -->
      <!-- Includes accordion -->
      <div class="d-flex flex-column min-vh-100 min-vw-100 justify-content-center align-items-center">

        <div class="accordion w-50" role="tablist">

          <!-- accordion v-for start: Using v-for through an object to fill out accordion content -->
          <b-card v-bind:key = "index" v-for = "(item, index) in details" no-body class="mb-1">
            <b-card-header header-tag="header" class="p-1" role="tab">
              <b-button block v-b-toggle = "'accordion-' + index" variant="info">{{item.title}}</b-button> <!-- updated button with data element & v-for -->
            </b-card-header>
            <b-collapse :id = "'accordion-' + index" visible accordion="my-accordion" role="tabpanel"> <!-- updated id with data element & v-for -->
              <b-card-body>
                <b-card-text>{{ item.content }}</b-card-text> <!-- updated text with data element & v-for -->
              </b-card-body>
            </b-collapse>
          </b-card>
          <!-- accordion v-for end: Using v-for through an object to fill out accordion content -->

        </div>
      </div>
      <!-- Accordion end -->
</template>

<script>
export default {
  head: {
  title: 'Travel Junkies blog',
  titleTemplate: '%s - Nuxt.js',
  meta: [
    { charset: 'utf-8' },
    { name: 'viewport', content: 'width=device-width, initial-scale=1' },

    // hid is used as unique identifier. Do not use `vmid` for it as it will not work
    { hid: 'description', name: 'description', content: 'Blog from the adventures of world travelers' }
    ]
  },
  name: 'AccordionPage',
  props: {
    msg: String
  },
//Passing repeated content
  data() {
  return {
    details:[
    {
        title: 'Accordion 1',
        content: 'Accordion 1 Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terryrichardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum eiusmod.'
    },
    {
        title: 'Accordion 2',
        content: 'Accordion 2 Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terryrichardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum eiusmod.'
    },
    {
        title: 'Accordion 3',
        content: 'Accordion 3 Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terryrichardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor brunch. Food truck quinoa nesciunt laborum eiusmod.'
    }
]
    //------Removing previous accordion text-------//
    // text: `
    //   Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus terry
    //   richardson ad squid. 3 wolf moon officia aute, non cupidatat skateboard dolor
    //   brunch. Food truck quinoa nesciunt laborum eiusmod.
    // `
  }
}
}
</script>

<style>
</style>
