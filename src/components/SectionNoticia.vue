<template>
  <div>
    <div class="row mt-md-5 mt-sm-5 mt-xs-5">
      <div
        class="col-lg-6 col-xs-12"
        v-for="(noticia, index) of noticias"
        :key="index"
      >
        <div class="card mb-3">
          <div class="row no-gutters">
            <div
              class="col-md-4 d-flex justify-content-center align-items-center"
            >
              <img
                :src="noticia.urlToImage"
                class="card-img"
                alt="Noticia image"
              />
            </div>
            <div class="col-md-8">
              <div class="card-body">
                <h5 class="card-title">{{ noticia.title }}</h5>
                <hr />
                <p class="card-text">
                  {{ noticia.description }}
                </p>
                <div class="row card-text">
                  <div class="col-md-9 justify-content-start">
                    <p class="card-text" style="color: #4529df">
                      Autor: {{ noticia.author }}
                    </p>
                  </div>
                  <div class="col-md-3 d-flex justify-content-end">
                    <a
                      :href="noticia.url"
                      target="_blank"
                      style="color: #556df4"
                      >Ir a</a
                    >
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "SectionNoticia",
  data() {
    return {
      noticias: null,
    };
  },
  mounted() {
    axios
      .get(
        "http://newsapi.org/v2/top-headlines?country=co&apiKey=b23cf0a36d1949d7ac9652f5e7930674"
      )
      .then((response) => {
        this.noticias = response.data.articles.slice(0, 4);
        console.log(this.noticias);
      });
  },
};
</script>