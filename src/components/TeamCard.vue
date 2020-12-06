<template>
  <div class="col-lg-3 col-md-6" style="margin-bottom: 20px">
    <div class="card shadow-lg TeamCards">
      <div class="card-body CardBody">
        <img
          v-bind:src="member.image"
          alt=""
          class="img-fluid shadow rounded-circle w-75 mb-3"
        />
        <div class="card-content">
          <h3>{{ member.nombre }}</h3>
          <p><b>Rol: </b>{{ member.rol }}</p>
          <p><b>Edad: </b>{{ member.edad }}</p>
          <p><b>Ocupacion: </b>{{ member.descripcion.ocupacion }}</p>
          <p><b>Residencia: </b>{{ member.descripcion.residencia }}</p>
          <p><b>Pasatiempos: </b>{{ member.descripcion.pasatiempos }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TeamCard",
  props: ["member"],
};
</script>

<style scoped>
.TeamCards {
  border-radius: 25px;
  background-color: #ffffff;
  background-image: linear-gradient(315deg, #ffffff 0%, #d7e1ec 74%);
  transition: 0.5s ease;
  margin-top: 50%;
}
.TeamCards:hover {
  color: #f1f1f1;
  background-color: #485461;
  background-image: linear-gradient(315deg, #485461 0%, #28313b 74%);
  transform: scale(1.1);
  cursor: pointer;
}
.TeamCards .card-content {
  margin-top: -40%;
}
.card-content h3 {
  font-size: 2rem;
}
.card-content p {
  padding: 0;
  line-height: 0.9rem;
  font-size: 0.85rem;
}
.TeamCards img {
  transform: translateY(-55%);
}
</style>
