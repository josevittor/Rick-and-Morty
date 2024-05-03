<script setup>
import { onMounted, reactive, ref } from 'vue';

defineProps([
    "personagem"
])

</script>

<template>
    <div class="col">
        <div class="card m-3">
            <div class="row g-0">
                <div class="col-md-4">
                    <img :src="personagem.image" class="img-fluid rounded-start" alt="...">
                </div>
                <div class="col-md-8">
                    <div class="card-body">
                        <h5 class="card-title">{{ personagem.name }}</h5>
                        <p class="card-text">
                            Status: {{ personagem.status }} <br>
                            Espécie: {{ personagem.species }} <br>
                            Gênero: {{ personagem.gender }} <br>
                            Local: {{ personagem.location.name }} <br>
                            Total De episódios: {{ personagem.episode.length }} <br>
                        </p>

                    </div>
                </div>
            </div>
        </div>
    </div>
</template>