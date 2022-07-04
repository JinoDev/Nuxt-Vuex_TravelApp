<template>
<div>
    <div v-if="pack" class="container py-5">
            <div class="hero-container">
                <img :src="require(`@/assets/images/${pack.image}`)" alt="city" class="image">
                <div class="info-box">
                    <h1>{{ pack.title }}</h1>
                    <p class="snippet">{{ pack.snippet }}</p>
                    <BookTrip
                    :pack="pack"
                    />
                </div>
            </div>
            <div class="whats-included-container">
                <div class="included-container">
                    <h6>Super Cool</h6>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, dolorem.</p>
                </div>
                <div class="included-container">
                    <h6>Super Awesome</h6>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, dolorem.</p>
                </div>
                <div class="included-container">
                    <h6>Super dope</h6>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, dolorem.</p>
                </div>
                <div class="included-container">
                    <h6>Super?</h6>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, dolorem.</p>
                </div>
            </div>
            <div class="description-container">
                <p>
                    {{ pack.description }}
                </p>
            </div>
           <Reviews/>
        </div>
        <div v-else class="container padding">
            <PageNotFound/>
        </div>
</div>

<!-- below id because that's what we called the dynamic file (if _hotdog.vue, then we'd say params.hotdog)-->
</template>

<script>

    export default {
        computed: {
          pack() {
              return this.$store.getters.getPackageId(this.$route.params.id)
          }
        }
    }
</script>

<style scoped>
.hero-container {
        display: flex;
        justify-content: space-between;
    }
    .image {
        width: 59%;
        height: 25rem;
        border-radius: 8px;
    }
    .info-box {
        width: 35%;
        background-color: #fcfcfc;
        padding: 1rem;
        padding-left: 2rem;
        border-radius: 0.5rem;
border-radius: 25px;
background: linear-gradient(315deg, #ffffff, #d6dcdd);
box-shadow:  -31px -31px 62px #dde3e5,
             31px 31px 62px #ffffff;
             /* display: flex;
             flex-direction: column;
             align-items: center; */
    }
    .info-box h1 {
        margin-top: 2rem;
    }
    .whats-included-container {
        border-bottom: 0.1rem solid rgba(128, 128, 128, 0.151);
    }
    .description-container {
        border-bottom: 0.1rem solid rgba(128, 128, 128, 0.151);
        padding-bottom: 2rem;
        margin-bottom: 2rem;
    }
    .included-container {
        margin-top: 1.5rem;
    }
    h1 {
        font-size: 1.75rem;
    }
    h6 {
        font-size: 1.15rem;
        font-weight: 400;
    }
    p {
        color: grey
    }
    .snippet {
        color: rgba(0, 0, 0, 0.774);
        margin-top: 1rem;
    }
    button {
        width: 100%;
        border: none;
        padding: 0.5rem;
        color: white;
        font-weight: 700;
        padding: 1rem 4rem;
        border-radius: 100rem;
        background-color: rgb(231, 81, 43);
        color: white;
        font-weight: 700;
        transition: 0.5s;
    }
    .description-container {
        margin-top: 3rem;
        color: grey
    }
    .padding {
        padding: 10rem 0
    }
</style>