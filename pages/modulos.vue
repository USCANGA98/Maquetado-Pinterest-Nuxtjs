<template>
  <div>
    <v-subheader>Home Page</v-subheader>
    <v-row>
      <v-col cols="3" v-for="(item, i) in items" :key="i">
        <imageCard
          :url="item.url"
          :meta="{ name: item.name, occupation: item.occupation }"
        />
      </v-col>
    </v-row>
  </div>
</template>

<script>
import imageCard from "../components/imageCard";
export default {
  data() {
    return {
      items: [
        {
          url:
            "https://images.unsplash.com/photo-1509130446053-899ae7358ce6?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjB8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",

          name: "Luis Angel",
          occupation: "Software Developer",
        },
        {
          url:
            "https://images.unsplash.com/photo-1509817775895-79efefb813d9?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mjh8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Mauricio Abad",
          occupation: "Supervisor",
        },
        {
          url:
            "https://images.unsplash.com/photo-1522258493909-bf27c8ebd64a?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjZ8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Ruben Fernndez",
          occupation: "Associate",
        },
        {
          url:
            "https://images.unsplash.com/photo-1522093243371-296c79a66df4?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MzF8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Adan Valle",
          occupation: "Executive",
        },
        {
          url:
            "https://images.unsplash.com/photo-1511407401960-0ee203836665?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MzJ8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Francisco Miguel Montoro",
          occupation: "Liason",
        },
        {
          url:
            "https://images.unsplash.com/photo-1542325828505-734937aa2040?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MzB8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Dario Fraile",
          occupation: "Officer",
        },
        {
          url:
            "https://images.unsplash.com/photo-1548623826-a1aa0a4d8a5b?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxzZWFyY2h8NDJ8fG1leGljb3xlbnwwfHwwfA%3D%3D&auto=format&fit=crop&w=400&q=60",
          name: "Juan Dios Granados",
          occupation: "Manager",
        },
        {
          url:
            "https://images.unsplash.com/photo-1520821586179-a7a385eb261a?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NTZ8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Luis Heredia",
          occupation: "Engineer",
        },
        {
          url:
            "https://images.unsplash.com/photo-1508979215797-e1249a67d9a1?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NTF8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Adolfo Monteagudo",
          occupation: "Specialist",
        },
        {
          url:
            "https://images.unsplash.com/photo-1580334317510-ccad4f66e249?ixid=MXwxMjA3fDB8MHxzZWFyY2h8OTF8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Mustapha Royo",
          occupation: "Director",
        },
        {
          url:
            "https://images.unsplash.com/photo-1591499182728-c66ba8220ccd?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTI5fHxtZXhpY298ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Carlos Javier Miguel",
          occupation: "Coordinator",
        },
        {
          url:
            "https://images.unsplash.com/photo-1563657296610-d0459418a7a7?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTQwfHxtZXhpY298ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Paulino Mari",
          occupation: "Administrator",
        },
        {
          url:
            "https://images.unsplash.com/photo-1495110265292-6a567e7246d5?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTQ5fHxtZXhpY298ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Jesus Miguel Ortega",
          occupation: "Architect",
        },
        {
          url:
            "https://images.unsplash.com/photo-1529733905113-027ed85d7e33?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80",
          name: "Ismael Campos",
          occupation: "Analyst",
        },
        {
          url:
            "https://images.unsplash.com/photo-1554710869-95f3df6a3197?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=325&q=80",
          name: "Antoni Reina",
          occupation: "Designer",
        },
        {
          url:
            "https://images.unsplash.com/photo-1512036594830-51cea3a8df78?ixid=MXwxMjA3fDB8MHxzZWFyY2h8N3x8bmVwYWx8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Aaron Rial",
          occupation: "Planner",
        },
        {
          url:
            "https://images.unsplash.com/photo-1523512090443-2d7df8b40358?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjF8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Gaspar Lopez",
          occupation: "Synergist",
        },
        {
          url:
            "https://images.unsplash.com/photo-1572253765558-ed6413a68da5?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MzR8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Andoni Ferre",
          occupation: "Orchestrator",
        },
        {
          url:
            "https://images.unsplash.com/photo-1592911843376-c86076523cc3?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mzd8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Ismael Amado",
          occupation: "Technician",
        },
        {
          url:
            "https://images.unsplash.com/photo-1553521756-74004ab1e8bd?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Njd8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Jose Joaquin Menendez",
          occupation: "Developer",
        },
        {
          url:
            "https://images.unsplash.com/photo-1552353288-5405ac4846f1?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NjV8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Luis Antonio Moron",
          occupation: "Producer",
        },
        {
          url:
            "https://images.unsplash.com/photo-1571401835393-8c5f35328320?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mnx8bmVwYWx8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Joel Barea",
          occupation: "Consultant",
        },
        {
          url:
            "https://images.unsplash.com/photo-1511215579272-6192432f83bc?ixid=MXwxMjA3fDB8MHxzZWFyY2h8OHx8bmVwYWx8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=700&q=60",
          name: "Julio Cesar Sancho",
          occupation: "Assistant",
        },
        {
          url:
            "https://images.unsplash.com/photo-1607662562783-9aeb834e23e5?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTl8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=700&q=60",
          name: "Mateo Souto",
          occupation: "Facilitator",
        },
        {
          url:
            "https://images.unsplash.com/photo-1541731290388-9860b1466aa6?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjJ8fG5lcGFsfGVufDB8fDB8&auto=format&fit=crop&w=400&q=60",
          name: "Hugo Saez",
          occupation: "Agent",
        },
        {
          url:
            "https://images.unsplash.com/photo-1500269062855-0d9c4410af0e?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjB8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Adan Olivera",
          occupation: "Representative",
        },
        {
          url:
            "https://images.unsplash.com/photo-1610423002339-340b7bbd8bfa?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjV8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Anton Vela",
          occupation: "Strategist",
        },
        {
          url:
            "https://images.unsplash.com/photo-1602992430520-105cf38b9e3e?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NDl8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Pedro Pablo Sanjuan",
          occupation: "doctor",
        },
        {
          url:
            "https://images.unsplash.com/photo-1542835435-4fa357baa00b?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTB8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Alexandre Bonilla",
          occupation: "plumber",
        },
        {
          url:
            "https://images.unsplash.com/photo-1572989994359-ae5afc3a3efe?ixid=MXwxMjA3fDB8MHxzZWFyY2h8OXx8bWV4aWNvfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Damian Alarcon",
          occupation: "artist",
        },
        {
          url:
            "https://images.unsplash.com/photo-1550815043-7fcead93a615?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTN8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Ion Correa",
          occupation: "cabalier",
        },
        {
          url:
            "https://images.unsplash.com/photo-1536266305399-b367feb671f9?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTd8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Josep Maria Zamorano",
          occupation: "runner's car",
        },
        {
          url:
            "https://images.unsplash.com/photo-1522092787785-60123fde65c4?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjF8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
          name: "Teofilo Ibañez",
          occupation: "Motorcyclist",
        },

        // "https://images.unsplash.com/photo-1522092787785-60123fde65c4?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjF8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1509817775895-79efefb813d9?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mjh8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1522258493909-bf27c8ebd64a?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjZ8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1522093243371-296c79a66df4?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MzF8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1511407401960-0ee203836665?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MzJ8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1542325828505-734937aa2040?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MzB8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1548623826-a1aa0a4d8a5b?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxzZWFyY2h8NDJ8fG1leGljb3xlbnwwfHwwfA%3D%3D&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1520821586179-a7a385eb261a?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NTZ8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1508979215797-e1249a67d9a1?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NTF8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1580334317510-ccad4f66e249?ixid=MXwxMjA3fDB8MHxzZWFyY2h8OTF8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1591499182728-c66ba8220ccd?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTI5fHxtZXhpY298ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1563657296610-d0459418a7a7?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTQwfHxtZXhpY298ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1495110265292-6a567e7246d5?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTQ5fHxtZXhpY298ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1529733905113-027ed85d7e33?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80",
        // "https://images.unsplash.com/photo-1554710869-95f3df6a3197?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=325&q=80",
        // "https://images.unsplash.com/photo-1512036594830-51cea3a8df78?ixid=MXwxMjA3fDB8MHxzZWFyY2h8N3x8bmVwYWx8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        // "https://images.unsplash.com/photo-1523512090443-2d7df8b40358?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjF8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        // "https://images.unsplash.com/photo-1572253765558-ed6413a68da5?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MzR8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        // "https://images.unsplash.com/photo-1592911843376-c86076523cc3?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mzd8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        // "https://images.unsplash.com/photo-1553521756-74004ab1e8bd?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Njd8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        // "https://images.unsplash.com/photo-1552353288-5405ac4846f1?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NjV8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        // "https://images.unsplash.com/photo-1571401835393-8c5f35328320?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mnx8bmVwYWx8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        // "https://images.unsplash.com/photo-1511215579272-6192432f83bc?ixid=MXwxMjA3fDB8MHxzZWFyY2h8OHx8bmVwYWx8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=700&q=60",
        // "https://images.unsplash.com/photo-1607662562783-9aeb834e23e5?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTl8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=700&q=60",
        // "https://images.unsplash.com/photo-1541731290388-9860b1466aa6?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjJ8fG5lcGFsfGVufDB8fDB8&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1500269062855-0d9c4410af0e?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjB8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1610423002339-340b7bbd8bfa?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjV8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1602992430520-105cf38b9e3e?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NDl8fG5lcGFsfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1542835435-4fa357baa00b?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTB8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1572989994359-ae5afc3a3efe?ixid=MXwxMjA3fDB8MHxzZWFyY2h8OXx8bWV4aWNvfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1550815043-7fcead93a615?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTN8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1536266305399-b367feb671f9?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTd8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
        // "https://images.unsplash.com/photo-1509130446053-899ae7358ce6?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjB8fG1leGljb3xlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
      ],
    };
  },
  components: {
    imageCard,
  },
};
</script>

<style lang="scss" scoped>
</style>