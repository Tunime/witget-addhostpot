<template>
   <div id="foradd" class="admin--edit">
        <h3 class="admin--edit--title">ADMIN-HOSTPOST</h3>
        <li class="admin--edit--btn">
            <a class="admin--edit--btn--btnaction" href="#">add hostpost</a>
        </li>
        <li class="admin--edit--btn">
            <a class="admin--edit--btn--btnaction" href="#">edit</a>
        </li>
        <div id="forinputs"></div>
        <li id="btnadd" class="admin--edit--add--btn" style="display: none;">
            <a @click="addhostpot" class="admin--edit--add--btnaction" href="#">Save</a>
        </li>
    </div>
</template>

<script>
export default {
  name: 'admin',
  data () {
    return {
      msg: 'no lo se rick'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.admin--edit{
        width: 20%;
        margin: 10px;
        background: rgb(255, 255, 255);
    }
        .admin--edit--title{
            text-align: center;
            padding: 1em;
        }
    .admin--view{
        width: 60%;
        margin: 10px;
        padding: 20px;
        background: #ffffff;
    }
        .admin--view--img{
            width: 100%;
        }
    .admin--edit--list{

    }
        .admin--edit--list--element{
            padding: 1em;
            margin: 0 0.7em 0.7em 0.7em;
            background: #ecf0f1;
        }
            .admin--edit--list--element--subtitle{
                font-weight: 400;
            }
    .admin--edit--btn{
        margin: 1em 0 0.5em 0;
        display: flex;
        justify-content: space-around;
    }
        .admin--edit--btn--btnaction{
            color: #fff;
            padding: 0.8em 10%;
            background: #3498db;
            border-radius: 5px;
            width: 100%;
            text-align: center;
            margin: 0 0.7em;
        }
        .admin--edit--btn--btnaction:hover{
            color: #fff;
            background: #2980b9;
        }
    .admin--edit--add{
        margin: 0 0.7em 0.7em 0.7em;
        display: flex;
        justify-content: space-around;
        flex-direction: column;
    }
        .admin__input{
            border: 1px solid #ced4da;
            border-radius: .25rem;
            padding: .375rem .75rem;
            margin: 0 0 0.5em 0;
            font-size: 0.9rem;
        }
</style>
