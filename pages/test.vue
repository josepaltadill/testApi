<template>
    <main>
        <h1>Pagina test</h1>
    </main>
</template>

<script>
export default {
    data() {
        const headers: new Headers(),
        headers.append('Authorization', 'Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE2MTIzNjQ5OTYsImF1ZCI6IjA3MTg2OTNkMTI1M2U3NDA3OGNjYWMxOGE0ZmYzMzU0NTEzNTAyM2MiLCJkYXRhIjp7InVzZXIiOiJyYXBpdGEiLCJwYXNzIjoidndrajgzelpEYSIsImtleVRlbXAiOiIuIn19.2StlzONp3Dmlrck9yvDDJuoDVz3x6vKHlpe6FMsdPNc'),
    
        headers.append('Content-Type', 'application/json'),

        body = {
            "idOperator": 4939,
            "typeElement": 2,
            "idElement": "10249",
            "idLanguage": 0
        },

        init = {
            method: 'POST',
            headers,
            body
        },
    },

    fetch('http://www.mrplan.es/scr/api/v1/public/operators/elements/get', init)
    .then((response) => {
    return response.json(); // or .text() or .blob() ...
    })
    .then((text) => {
    // text is the response body
    })
    .catch((e) => {
    // error in e.message
    });
}
</script>