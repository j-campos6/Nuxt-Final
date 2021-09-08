<template>
 <div>
   <b-card-group deck >
     <b-card
       border-variant="secondary"
       :header="'Country: ' + country.name "
       header-border-variant="secondary"
       align="center"
     >
       <b-card-text>Currency:  {{country.currencies[0].code}} ( {{country.currencies[0].name}})</b-card-text>
     </b-card>
   </b-card-group>

 </div>


</template>

<script>
export default {
	props: {
		country: Object
	}
}
</script>


<style>

</style>
