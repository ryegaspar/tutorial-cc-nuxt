<template>
    <p>{{ posts }}</p>
</template>

<script>
    import axios from 'axios';

    export default {
    	data() {
    		return {
    			posts: []
            }
        },

        async asyncData() {
    		let response = await axios.get('https://jsonplaceholder.typicode.com/posts')

            return {
    			posts: response.data
            }
        }

        // asyncData() {
    	// 	return axios.get('https://jsonplaceholder.typicode.com/posts').then((response) => {
    	// 		return {
    	// 			posts: response.data
        //         }
        //     });
        // }


    }
</script>