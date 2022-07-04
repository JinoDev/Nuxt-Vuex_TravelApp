<template>
    <nav class="navbar navbar-expand-lg navbar-dark padding">
    <NuxtLink class="navbar-brand" to="/">Blablatrip</NuxtLink>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse ml-auto" id="navbarSupportedContent">
        <ul class="navbar-nav ml-auto">
            <li class="nav-item active">
                <NuxtLink to="/packages" class="nav-link">Packages <span class="sr-only">(current)</span></NuxtLink>
            </li>
            <li class="nav-item active">
                <NuxtLink to="/my-trips" class="nav-link">My Trips <span class="sr-only">(current)</span></NuxtLink>
            </li>
        </ul>
    </div>
    </nav>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.nav-link {
    margin-right: 3rem;
}
  .padding {
        padding: 1.5rem;
        background-color: #354259;
    }
    .nav-left {
        margin-left: auto;
    }
</style>