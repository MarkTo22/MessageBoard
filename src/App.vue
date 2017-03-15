<template>
  <div class="container">
    <app-header :maxQuotes="maxQuotes" :quoteCount="quotes.length"></app-header>
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue'
import NewQuote from './components/NewQuote.vue'
import Header from './components/Header.vue'


export default{
  data(){
    return {
      quotes:[
        'Just a quote to see something'
      ],
      maxQuotes:10
    }
  },
  methods:{
    newQuote(quote){
      if(this.quotes.length>=this.maxQuotes){
        return alert('too much');
      }
      this.quotes.push(quote);
    },
    deleteQuote(index){
      this.quotes.splice(index,1);
    }
  },
  components:{
    appQuoteGrid:QuoteGrid,
    appNewQuote:NewQuote,
    appHeader:Header
  }
}
 
</script>

<style>
 
</style>