<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <br>
                <button class="btn btn-primary"
                        @click="selectedComponent='appBlue'">
                  Load Blue Template
                </button>
                <button class="btn btn-success"
                        @click="selectedComponent='appGreen'">
                  Load Green Template
                </button>
                <button class="btn btn-danger"
                        @click="selectedComponent='appRed'">
                  Load Red Template
                </button>
                <hr>
                <p>{{ selectedComponent }}</p>
                <hr>
                <component :is="selectedComponent">
                  <p>
                    Lorem impusium dafta lema kaermen summi
                  </p>
                </component>
                <!--app-blue>
                  <h1>My blue section</h1>
                  <p>
                    Lorem impusium dafta lema kaermen summi
                  </p>
                </app-blue>
                <app-green>
                  <h1>My GREEN section</h1>
                  <p>
                    Lorem impusium dafta lema kaermen summi
                  </p>
                </app-green>
                <app-red>
                  <h1>My ReD section</h1>
                  <p>
                    Lorem impusium dafta lema kaermen summi
                  </p>
                </app-red-->
            </div>
        </div>
    </div>
</template>

<script>
    import Blue from './components/Blue.vue';
    import Green from './components/Green.vue';
    import Red from './components/Red.vue';

    export default {
        data: function() {
          return {
            selectedComponent: 'appBlue'
          };
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
