<template>
    <div>
        <AppHeader/>
        <div class="container">
            <h1 class="hello">Hello World</h1>
            <p class="about-the-site">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Est ducimus numquam consequuntur qui modi voluptate veniam. Eum eos ratione accusantium molestias dignissimos hic, incidunt odit unde fuga harum quod? Ipsum est impedit ab quo? Quam, ex laudantium repellendus quia sapiente deleniti accusamus iure deserunt, autem dolore cumque nostrum blanditiis non laboriosam expedita delectus sequi, temporibus aut soluta. Atque doloremque consequuntur autem enim neque tempora earum suscipit porro. Reprehenderit, tempore voluptates adipisci dignissimos accusantium eum optio cumque praesentium hic velit labore impedit quos sapiente sed similique maiores repellat natus possimus ducimus eligendi est commodi voluptate consectetur porro! Voluptate, numquam aut, esse non voluptatum magnam illo labore quaerat modi iste possimus! Dolore est voluptatum molestiae minima fugiat aperiam temporibus voluptate, laudantium vel dolor laborum officiis. Laborum, rerum numquam. Sunt doloribus illum, libero aliquam minima culpa assumenda iusto eaque tempora voluptatum molestias officia vitae impedit quis, beatae voluptas unde consequuntur laudantium obcaecati, deserunt labore non eos molestiae deleniti! Possimus ea magnam quos doloribus sint hic non ipsa voluptatum vero odit provident deserunt, a culpa. Voluptatem placeat, optio amet suscipit vitae rem non, dignissimos mollitia praesentium, esse laborum distinctio ea sed sint ut? Debitis quia veritatis optio at sequi. Beatae veritatis velit sapiente culpa, dolores nisi quas pariatur possimus debitis fugiat non fugit quasi commodi. Rerum, veritatis itaque quae officiis, hic doloribus suscipit eum necessitatibus excepturi, enim tempora. Dicta rerum optio nemo pariatur inventore unde, aspernatur exercitationem eaque sunt ut voluptas iste aliquid, quisquam sit doloremque. Ad beatae tempora doloremque aut, architecto temporibus at odio voluptate eligendi saepe quas dolores nostrum, distinctio explicabo nobis adipisci, alias reiciendis illo rem nihil sit harum laboriosam illum. Nulla, est aperiam soluta a veniam illo fugit quos sapiente, dolor sint quia nemo cupiditate! Numquam, molestias iure eveniet maiores facilis sit eligendi minus, dignissimos nostrum velit vero fuga non.</p>
        </div>
    </div>
</template>

<script>
import AppHeader from './../components/AppHeader.vue'
export default {
  components: { AppHeader },

}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');
*{
    padding: 0;
    margin: 0;
    box-sizing: inherit;
}
body{
    background: rgba(141, 139, 139, 0.952);
    font-family: 'Roboto', sans-serif;
}
.hello{
    text-align: center;
    margin-top: 20px;
    color: rgb(214, 218, 219);
}
.about-the-site{
    text-align: center;
    padding: 25px;
    font-size: 1.1rem;
    color: rgb(214, 218, 219);
    
}
</style>>
