<template>
  <div class="item">
    <i>
      <slot name="icon"></slot>
    </i>
    <div class="details">
      <h3>
        <slot name="heading"></slot>
      </h3>
      <slot></slot>
    </div>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Comfortaa&family=Libre+Franklin:wght@300&display=swap" rel="stylesheet');

* {
    --orangelight: #ffa364;
    --pomegranate: #eb3e1b;
    --orangelighting: #fb6d10;
    --darkorange: #fc7643;
    --orange: #af4f41;
    --navblue: #273248;
    --blue: #2e2e41;
    --cream: #ffebd2;
    font-family: "Comfortaa", cursive;
    font-family: "Libre Franklin", sans-serif;
}

body{
    background-color: var(--cream);
    overflow-x: hidden;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

.navbar{
    background-color: var(--orangelighting);
    width: 100vw;
}

.navbar .logo{
    width: 7%;
}

.busqueda{
    background-color: var(--cream);
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 3rem;
    width: 100vw;
}

.busqueda input{
    margin-top: 35px;
    border-radius: 25px;
    border-color: var(--blue);
    border-width: 2.5px;
    width: 500px;
    height: 50px;
    font-family: 'Comfortaa';
}

.busqueda label{
    margin-top: 20px;
    font-family: 'Comfortaa';
    font-size: 30px;
}

.icons-busqueda {
    display: flex;
    justify-content: center;
    margin-top: 40px;
}

.icons-busqueda a{
    text-decoration: none;
    color: black;
}

.icons-busqueda span i{
    font-size: 50px;
    padding-left: 60px;
    padding-right: 30px;
}

/*.icons-busqueda a img{
    width: 145px;
    padding-left: 60px;
    padding-right: 30px;
    margin-bottom: 6px;
} */

.icons-busqueda .label-icon-busqueda{
    font-family: 'Comfortaa';
    font-size: 18px;
}

.footer-inicio{
    background: var(--navblue);
    margin-top: auto;
}

.content-inicio{
    display: flex;
    flex-wrap: wrap;
    margin: 0;
    padding: 30px;
    width: 100vw;
    justify-content: center;
}

.content-inicio .card{
    width: 230px;
    height: 330px;
    border-radius: 8px;
    box-shadow: 0 2px 2px var(--blue);
    overflow: hidden;
    margin: 10px;
    text-align: center;
    transition: all 0.25s;
    background: var(--orangelighting);
}

.content-inicio .card img{
    width: 500px;
    height: 200px;
}

.content-inicio .card .card-title{
    font-family: 'Comfortaa';
}

.content-inicio .card .card-body{
    font-family: 'Comfortaa';
}

.footer-inicio a{
    text-decoration: none;
    color:white;
    font-family: 'Comfortaa';
}

.footer-inicio hr{
    color: var(--cream)
}
.item {
  margin-top: 2rem;
  display: flex;
}

.details {
  flex: 1;
  margin-left: 1rem;
}

i {
  display: flex;
  place-items: center;
  place-content: center;
  width: 32px;
  height: 32px;
  color: var(--color-text);
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
}

@media (min-width: 1024px) {
  .item {
    margin-top: 0;
    padding: 0.4rem 0 1rem calc(var(--section-gap) / 2);
  }

  i {
    top: calc(50% - 25px);
    left: -26px;
    position: absolute;
    border: 1px solid var(--color-border);
    background: var(--color-background);
    border-radius: 8px;
    width: 50px;
    height: 50px;
  }

  .item:before {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    bottom: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:after {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    top: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:first-of-type:before {
    display: none;
  }

  .item:last-of-type:after {
    display: none;
  }
}
</style>
