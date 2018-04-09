<template>
   <div id="witget" class="admin--view">
      <a id="witgetimg" @click="newhospot">
          <img class="admin--view--img" src="https://respuestas.tips/wp-content/uploads/2015/04/sistema-solar-planetas.jpg" alt="">
      </a>
  </div>
</template>

<script>
export default {
  name: 'witget',
   data(){
            datoss: localStorage.getItem("istitlekey").length
  },
  created(){
      var datos=JSON.parse(localStorage.getItem("istitlekey"));
      render(datos);
      function render (datos) {
          var html = datos.map(function(elem, index) {
            return('<div id="posts" style="top:'+elem.scaleY+'px; left:'+elem.scaleX+'px;"></div>');
        }).join(" ");
        $('#witgetimg').append(html);
      }
  },
  methods:{
      newhospot:function(event){
          $("#btnadd").css("display", "block");
          $('#forinputs').append('<div id="alvarus" class="admin--edit--add"><input id="scaley" type="text" class="admin__input" value="'+event.clientY+'"><input id="scalex" type="text" class="admin__input" value="'+event.clientX+'"><input id="mstitle" type="text" class="admin__input" placeholder="Title"><input id="mssubtitle" type="text" class="admin__input" placeholder="Subtitle"><textarea id="msdescription" class="admin__input" id="exampleFormControlTextarea1" rows="3" placeholder="Descripcion"></textarea><input id="msurl" type="text" class="admin__input" placeholder="img URL"></div>');
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
    background: #1ABC9C;
    border-radius: 50%;
    cursor: pointer;
    z-index: 200;
    margin-left: -10px;
    margin-top: -10px;
    }
</style>
