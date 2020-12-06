<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-light bg-secondary">
      <a class="navbar-brand" href="#">
        <img
          src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e7/Instagram_logo_2016.svg/768px-Instagram_logo_2016.svg.png"
          width="30"
          height="30"
          class="text-white d-inline-block align top"
          alt=" "
          loading="lazy"
          style="margin-right: 10px"
        />Desarrollo de talento digital - Equipo 117
      </a>

      <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item active">
            <a class="nav-link text-white" href="#"
              >Inicio <span class="sr-only">(current)</span></a
            >
          </li>

          <li class="nav-item">
            <a class="nav-link text-white" href="#services">Servicios </a>
          </li>

          <li class="nav-item">
            <a class="nav-link text-white" href="#news">Noticias </a>
          </li>

          <li class="nav-item">
            <a class="nav-link text-white" href="#teams">Miembros </a>
          </li>
        </ul>
      </div>
    </nav>

    <div
      id="carouselExampleCaptions"
      class="carousel slide"
      data-ride="carousel"
    >
      <ol class="carousel-indicators">
        <li
          data-target="#carouselExampleCaptions"
          data-slide-to="0"
          class="active"
        ></li>
        <li data-target="#carouselExampleCaptions" data-slide-to="1"></li>
        <li data-target="#carouselExampleCaptions" data-slide-to="2"></li>
      </ol>

      <div class="carousel-inner">
        <div class="carousel-item active bg-light">
          <img
            class="d-block w-100 cortar"
            src="https://placeimg.com/1000/480/animals"
            alt="Responsive image"
          />
          <div class="carousel-caption d-none d-md-block">
            <h5 class="text-white">Animales sorprendentes</h5>
            <p class="text-white">Descubre sitios únicos y maravillosos</p>
          </div>
        </div>

        <div class="carousel-item bg-light">
          <img
            class="d-block w-100 cortar"
            src="https://placeimg.com/1000/480/nature"
            alt="Responsive image"
          />
          <div class="carousel-caption d-none d-md-block">
            <h5 class="text-white">Naturaleza por explorar</h5>
            <p class="text-white">Descubre sitios únicos y maravillosos</p>
          </div>
        </div>

        <div class="carousel-item bg-light">
          <img
            class="d-block w-100 cortar"
            src="https://placeimg.com/1000/480/arch"
            alt="Responsive image"
          />
          <div class="carousel-caption d-none d-md-block">
            <h5 class="text-white">Arquitectura fascinante</h5>
            <p class="text-white">Descubre sitios únicos y maravillosos</p>
          </div>
        </div>

        <a
          class="carousel-control-prev bg-light"
          href="#carouselExampleCaptions"
          role="button"
          data-slide="prev"
        >
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="sr-only">Previous</span>
        </a>
        <a
          class="carousel-control-next bg-light"
          href=" #carouselExampleCaptions"
          role="button"
          data-slide="next"
        >
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="sr-only">Next</span>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionMenu",
  props: ["member"],
};
</script>

<style scoped>
.cortar {
  overflow: hidden;
  max-height: 400px;
  object-fit: cover;
}
</style>