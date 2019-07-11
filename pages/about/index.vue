<template>
    <div class="app">
        <div class="container py-5 text-center">
            <div class="col-lg-12 col-sm-12 col-md-12 justify-content-center d-flex">
                <img src="https://images.unsplash.com/photo-1503443207922-dff7d543fd0e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=564&q=80" width="200" height="200" class="rounded-circle" alt="Cinque Terre">
            </div>
            <h1 class="py-5 title">Your Name</h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ea, quae culpa. Laboriosam sit iusto, eligendi vero praesentium quaerat sint reiciendis mollitia consequuntur natus at consectetur magnam repellat? Eos, quo dignissimos.</p>
        </div>
    </div>
</template>

<script>
export default {
    head(){
        return{
            title:'About',
            meta: [
                {
                    hid:'description',
                    meta:'description',
                    content: 'put your content here'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.app {
    background-color: rgb(61, 0, 160);
    color: white;
    p {
        font-size: 1.5em;
        font-weight: 200;
    }
    padding: 9%;
}
</style>
