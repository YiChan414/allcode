<template>
        <div>
            <ul>
                <li v-for="m in messageList" :key="m.id">
                    
                        <router-link :to="`/home/message/detail/${m.id}/${m.title}`">{{m.title}}</router-link>
                    

                    
                </li>
            </ul>
        <hr>
            <router-view></router-view>
        </div>
</template>

<script>
export default {
    name:'Message',
     data(){
        return{
            messageList:[
                {id:'001',title:'消息1'},
                {id:'002',title:'消息2'},
                {id:'003',title:'消息3'}
            ]
        }
    }
}
</script>

<style>

</style>