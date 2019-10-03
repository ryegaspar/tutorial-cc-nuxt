<template>
    <div class="container">
        <div class="row">
            <div class="col-md-8">
                <nuxt/>
            </div>
            <div class="col-md-4">
                <client-only><!-- anything wrapped in client-only, will not be rendered in server side -->
                    <v-select placeholder="Select category" :options="['foo', 'bar']"></v-select>
                </client-only>
            </div>
        </div>
    </div>
</template>