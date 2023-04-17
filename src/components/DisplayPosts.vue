<template>
    <section>
        <h1>Posts</h1>
        <button @click="toggle_posts">Toggle</button>
       <div class="main_card">
        <article  v-for="(post, i) in posts" :key="i" >
            <p>{{post[`content`]}}</p>
            <p>{{post[`user`]}}</p>
            <p>{{ post[`date_created`]}}</p>
        </article>
       </div>
    </section>
</template>

<script>
    export default {

        data() {
            return {
                change_layout:true,
                posts :[
                    {
                        content: 'The "Sakura" flower, also known as the cherry blossom, is a symbol of beauty, love, and renewal in Japanese culture.',
                        user: 'Hiroshi Nakamura',
                        date_created: 'April 12, 2023'
                    },
                    {
                        content: 'The "Zahara" flower, also known as the desert rose, is a beautiful and resilient flower that thrives in hot and dry climates.',
                        user: 'Sanaa Hassan',
                        date_created: 'April 11, 2023'
                    },
                    {
                        content: 'The "Anthurium" flower, also known as the flamingo flower, is a tropical flower with a unique shape and vibrant colors.',
                        user: 'Juan Carlos Rodriguez',
                        date_created: 'April 10, 2023'
                    },
                    {
                        content: 'The "Protea" flower, also known as the sugarbush, is a stunning flower native to South Africa that is often used in floral arrangements.',
                        user: 'Lindiwe Mbatha',
                        date_created: 'April 9, 2023'
                    },
                    {
                        content: 'The "Orchid" flower is a delicate and exotic flower that comes in many different shapes, sizes, and colors.',
                        user: 'Lin Mei',
                        date_created: 'April 8, 2023'
                    },
                    {
                        content: 'The "Frangipani" flower, also known as the plumeria, is a tropical flower that is often used in Hawaiian leis and symbolizes love and devotion.',
                        user: 'Kai Lee',
                        date_created: 'April 7, 2023'
                    }
                ]
            }
    },
    methods: {
        toggle_posts: function (){
            let get_card = document.querySelector( '.main_card' )
            let get_toggled = document.querySelector('.toggled')

            if ( this.change_layout === true ){
                get_card.classList.add('toggled')
                get_card.classList.remove('main_card')
            
            } else{
                get_toggled.classList.add( 'main_card' )
                get_toggled.classList.remove('toggled')
            }
            this.change_layout =!this.change_layout 

        }
    }
    }
</script>

<style scoped>
section{
    display:grid;
    place-items: center;
    min-height: 80vh;
    padding: 16px;
}
h1{
    color:red;
    justify-self: start;
}
button{
  width: 192px;
  background-color: #79adde;
  border: none;
  border-radius: 25px;
  color: white;
  font-weight: 700;
  padding: 7px;
  transition: background-color 0.5s ease;
  box-shadow: 0 3px 0 #afcce7;

}
button:active{
    transform: translateY(3px);
  box-shadow: none;
}
.main_card{
    display:grid;
    place-items: center;
    min-height: 100vh;
}
.toggled{
    display:grid;
    place-items: center;
    grid-template-columns:1fr 1fr 1fr;
    min-height: 100vh;
}
article{
    display:grid;
    place-items: center;
    background-color: lightblue;
    margin: 16px;
    width: 80%;
    padding: 16px;
}
p{
    text-align: start;
    padding: 6px;
    font-weight: 700;

}

</style>