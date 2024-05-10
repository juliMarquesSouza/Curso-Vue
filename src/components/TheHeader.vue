  <template>
    <div class="container">
      <header>
       <h1 :class="{'title': true, 'title-home': isHome}">
        Curso Vue 3
       </h1>

       <p :class="pClass">
        Placehold is a simple, fast and free image placeholder service to generate SVG, PNG, JPEG and WebP placeholder images for your project.
       </p>
       
      </header>

        <div
            v-for="obj in todos"
            v-bind:key="obj.id"
            class="todos-item"
        >
          <div class="container_img">
            <img v-bind:src="obj.imgSrc">
          </div>
          {{ index }} {{ obj.title }}
        </div>
    </div>
</template>

<script>
    export default {
        name: 'TheHeader',
        data() {
            return {
                isHome: true,
                classVar: 'title',
                imgAlt: 'Foto de Jon Snow',
                pClass: 'text',
                todos: [
  {
    "userId": 1,
    "id": 1,
    "title": "1 - delectus aut autem",
    "completed": false,
    "imgSrc": 'https://placehold.co/600x400/png',
  },
  {
    "userId": 1,
    "id": 2,
    "title": "2 - quis ut nam facilis et officia qui",
    "completed": false,
    "imgSrc": 'https://placehold.co/600x400/png',
  },
  {
    "userId": 1,
    "id": 3,
    "title": "3 - fugiat veniam minus",
    "completed": false
  },
  {
    "userId": 1,
    "id": 4,
    "title": "4 - et porro tempora",
    "completed": true
  },
  {
    "userId": 1,
    "id": 5,
    "title": "5 - laboriosam mollitia et enim quasi adipisci quia provident illum",
    "completed": false
  },
]
            }
        }

    }
</script>

<style>
header {
  width: 50rem;
  padding: 3px 6px;
  display: block;
  text-align: left;
}

.text{
  color: black;
}
.title{
  font-size: 20px;
  color: blue;

}
    .container{
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      width: 100%;
    }
  
.title-home {
  font-size: 40px;
  color: green;
}
    .todos-item {
        background: #000;
        margin: 0 0 5px 0;
        padding: 3px 6px;
        color: #fff;
        width: 50rem;
        display: flex;
        align-items: flex-end;
        gap: 1rem;

    
        
    }
    .todos-item .container_img{
      display: flex;
      width: 20rem;
      height: 10rem;
    }
    .container_img img {
      display: flex;
      width: 100%;
    }
</style>

