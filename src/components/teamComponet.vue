<template>
  <div>
    <h2>The best teams of soccer in the world.</h2>

    <table class="table">
      <!--v-if="teams"-->
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">Name</th>
          <th scope="col">City</th>
          <th scope="col">Captain</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="team in teams" :key="team.id">
          <th scope="row">{{team.id}}</th>
          <td>{{ team.nombre }}</td>
          <td>{{ team.ciudad }}</td>
          <td>{{ team.capitan }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
<script>
import axios from "axios";

export default {
  name: "teamComponent",
  components: {},
  data: () => ({
    name: "Daniel",
    teams: [],
  }),
  mounted() {
    this.getTeams();
  },

  methods: {
    getTeams() {
      axios
        .get("http://127.0.0.1:8000/api/equipos")
        .then((res) => {
          //if (res.statusText == "success") {
          this.teams = res.data;
          console.log(this.teams);
          //console.log("hello");
          //}

          // console.log(res);
        })
        .catch((error) => {
          console.log(error);
        });
      /*  fetch('http://127.0.0.1:8000/api/equipos')
        .then((response) => response.json())
        .then((res) => {
          console.log(res);
        })
        .catch((err) => console.log(err));   */

      /* axios
        .get("http://127.0.0.1:8000/api/equipos")
        .then((res) => console.log(res.data)); */
    },
  },
};
//private url: string = 'http://127.0.0.1:8000/api';

/* headers = new HttpHeaders({
        'Content-Type': 'application/json',
        'Access-Control-Allow-Origin': '*',
        'Access-Control-Allow-Methods': 'GET, POST, PATCH, PUT, DELETE, OPTIONS',
        'Access-Control-Allow-Headers': 'Origin, Content-Type, X-Auth-Token',
    }); */

//SERVICIOS  DE EQUIPOS
/* getEquipos(endpoint) {
        let headers = this.headers;
        return this.http
            .get(`${this.url}/${endpoint}`, { headers })
            .toPromise()
            .then((response: any) => response);
    }
    borrarEquipo(id: any) {
        return this.http.delete(`${this.url}/equipos/${id}`);
    }
 */
</script>

<style></style>
