<template>
<div>
  <p>{{$t('message')}} </p>
  <p>{{$t("email", {email})}}</p>
  <p>{{$t('goodbye',{name})}} </p>

  <p>{{$tc("car",1)}}</p> 
  <p>{{$tc("car",3)}}</p>


  <p>{{$tc("person",0)}}</p>
  <p>{{$tc("person",1)}}</p>
  <p>{{$tc("person",4)}}</p>

  <p>{{$tc("apples",0)}}</p>
  <p>{{$tc("apples",1)}}</p>
  <p>{{$tc("apples",4)}}</p>

  <p>{{$n(100,"currency")}} </p>


  <h3> {{$d(new Date(),"long")}} </h3>
  <h3> {{$d(new Date(),"long","en-GB")}} </h3>


  <button @click="setLocale('en')" class="button">English</button>
  <button @click="setLocale('es')" class="button">Spanish</button>
  <button @click="setLocale('hr')" class="button">Hrvatski</button>


  </div>
</template>

<script>
export default {
  name: 'HelloI18n',
  data(){
    return{
      name:"ivvvcdcdo",
      email: "ivo.bagaric.2@gmail.com"
    }
  },
  methods:{
    setLocale(locale){
      this.$i18n.locale=locale
      localStorage.setItem("locale",locale)
    }
  }
}
</script>

