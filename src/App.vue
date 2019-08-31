<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <br>
                <button class="btn btn-primary" @click="selectedComp = 'app-blue'" >Load Blue Template</button>
                <button class="btn btn-success" @click="selectedComp = 'app-green'">Load Green Template</button>
                <button class="btn btn-danger" @click="selectedComp = 'app-red'">Load Red Template</button>
                <hr>
				<component :is="selectedComp">
					<h1>Dynamic Baby!</h1>
				</component>

            </div>
        </div>
    </div>
</template>

<script>
    import Blue from './components/Blue.vue';
    import Green from './components/Green.vue';
    import Red from './components/Red.vue';

    export default {
		data: function (){
			return {
				selectedComp: 'app-blue'
			}
		},
        components: {
            appBlue: Blue,
            appGreen: Green,
            appRed: Red
        }
    }
</script>

<style>
</style>
