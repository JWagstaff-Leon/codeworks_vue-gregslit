<template>
    <div class="offcanvas offcanvas-start" tabindex="-1" id="listings-menu">
        <div class="offcanvas-header">
            <h5 class="offcanvas-title">Gregs'List</h5>
            <button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas" aria-label="Close"></button>
        </div>
        <div class="offcanvas-body p-0 mt-4">
            <ul class="list-group list-group-flush">
                <button class="list-group-item list-group-item-action" @click="navigate('Cars')">Afforable Cars</button>
                <button class="list-group-item list-group-item-action" @click="navigate('Houses')">Modern Homes</button>
                <button class="list-group-item list-group-item-action" @click="navigate('Jobs')">Competitive Jobs</button>
            </ul>
        </div>
    </div>
</template>

<script>
import { Offcanvas } from 'bootstrap'
import { useRouter } from 'vue-router'
export default
{
    setup()
    {
        const router = useRouter();
        return {
            navigate(name)
            {
                Offcanvas.getOrCreateInstance(document.getElementById("listings-menu")).hide()
                router.push({name})
            }
        }
    }
}
</script>

<style lang="scss" scoped>

</style>