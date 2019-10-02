<template>
    <div>
        <post :post="post"></post>
    </div>
</template>

<script>
    import axios from 'axios';
    import Post from '@/components/Post';

    export default {
    	data() {
    		return {
    			post: null,
            }
        },

        head() { //for dynamic titles, use this format
    		return {
    			title: this.post.title
            }
        },

        components: {
    		Post
        },

    	async asyncData ( {params} ) {

    		// console.log(params);
    		let response = await axios.get(`https://jsonplaceholder.typicode.com/posts/${params.id}`);

    		return {
    			post: response.data
            }

        }
    }
</script>