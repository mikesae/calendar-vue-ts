<script lang="ts">
    import { FullCalendar } from 'vue-full-calendar';
    import Vue from 'vue';
    import Component from 'vue-class-component';

    @Component({
        components: {
            FullCalendar,
        },
        template: '<CalendarWrap :config="config" :events="events"/>',
    })
    export default class Calendar extends Vue {
        public config = {
            defaultView: 'month',
            header: {
                left: 'today',
                center: 'title',
                right: 'prev,next',
            },
        };
        public events = [
            {title: 'Pasta Faggioli', start: '2018-04-18'},
            {title: 'Burgers', start: '2018-04-19'},
            {title: 'Pizza', start: '2018-04-20'},
        ];
    }
</script>

<style>
    @import '../../node_modules/fullcalendar/dist/fullcalendar.css';
</style>
