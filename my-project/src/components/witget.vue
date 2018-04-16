<template>
   <div id="witget" class="admin--view">
      <a id="witgetimg" @click="newhospot">
          <div v-for="hostpot in hostpots">
            <div id="posts" v-bind:style="{top:hostpot.scaleY+'px', left:hostpot.scaleX+'px'}">
              {{hostpot.sid}}
            </div>
              <div v-bind:style="{top:hostpot.scaleY+'px', left:hostpot.scaleX+'px'}" class="card">
                <h2>{{hostpot.stitle}}</h2>
                <h3>{{hostpot.ssubtitle}}</h3>
                <p>{{hostpot.sdescription}}</p>
                <div class="firure">
                <img class="admin--view--img" v-bind:src="hostpot.surl" alt="">
              </div>
            </div>
          </div>
          <img class="admin--view--img" src="https://respuestas.tips/wp-content/uploads/2015/04/sistema-solar-planetas.jpg" alt="">
      </a>
  </div>
</template>

<script>
export default {
  name: 'witget',
   data(){
      return {hostpots: JSON.parse(localStorage.getItem("istitlekey"))}
  },

  methods:{
      newhospot:function(event){
          $("#btnadd").css("display", "flex");
          $('#forinputs').append('<div id="alvarus" class="admin--edit--add"><input style="display: none;" id="scaley" type="text" class="admin__input" value="'+event.clientY+'"><input style="display: none;" id="scalex" type="text" class="admin__input" value="'+event.clientX+'"><input id="mstitle" type="text" class="admin__input" placeholder="Title"><input id="mssubtitle" type="text" class="admin__input" placeholder="Subtitle"><textarea id="msdescription" class="admin__input" id="exampleFormControlTextarea1" rows="3" placeholder="Descripcion"></textarea><input id="msurl" type="text" class="admin__input" placeholder="img URL"></div>');
          $('#witgetimg').append('<div id="posts" style="top:'+event.clientY+'px; left:'+event.clientX+'px;"></div>');

      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.admin--view{
        width: 60%;
        margin: 10px;
        padding: 20px;
        background: #ffffff;
    }
        .admin--view--img{
            width: 100%;
        }
  #posts{
    height: 20px;
    width: 20px;
    position: absolute;
    background: #F9B326;
    border-radius: 50%;
    cursor: pointer;
    z-index: 200;
    margin-left: -10px;
    margin-top: -10px;
    color: #424242;
    text-align: center;
    padding: 0.5em;
    }
    #posts:hover + .card{
    display: block;
}
.card{
    display: none;
    background: #fff;
    position: absolute;
    width: 300px;
    height: 300px;
    padding: 20px;
    border: solid 2px #F9B326;
    color: #424242;
    font-size: 16px;
    margin-left: -10px;
    margin-top: -10px;
    z-index: 300;
    margin: 0 0 0 1.5em;
    overflow: scroll;
}
.card:hover{
    display: block;
}
.card img{
    width: 100%;
}
</style>
