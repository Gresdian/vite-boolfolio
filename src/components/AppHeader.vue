<script>
import { store } from '../store.js';

export default {
    data() {
        return {
            store,
        }
    }, 
}
</script>
<template lang="">
    <header>
        <div class="container">
            <div class="row">
                <div class="col-4">
                    <h4>Boolfolio</h4>
                </div>  
                <div class="col-8">
                    <div class="float-end">
                        <ul class="list-unstyled d-flex align-items-center">
                            <li v-for= "item, index in store.menuItems" :key="index">
                                <router-link :to="{ name: item.name }">{{ item.label }}</router-link>
                            </li>
                        </ul>        
                    </div>
                </div>   
            </div>    
        </div>    
    </header>
</template>
<style lang="scss" scoped>
  header{
    background-color: lightslategray;
    padding: 20px 0px;

    ul{
        li{
            padding: 5px 15px;

            a{
                color: #fff;
                text-decoration: none;

                &:hover {
                    color: darkslategray;
                }
            }
        }
    }
  }
    
</style>