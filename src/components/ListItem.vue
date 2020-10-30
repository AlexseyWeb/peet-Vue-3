<template>
    <div class="list-item" @click="favoriteItem(list.id)">
        <div class="user-profile__item">
            <div class="list-item__user">
                @{{ username }}
            </div>
            <div class="list-item__content">
                {{ list.content }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "ListItem",
    props: {
        username: {
            type: String,
            required: true,
        },
        list: {
            type: Object,
            required: true
        }
    },
    methods: {
        favoriteItem(id){
            this.$emit('favorite', id)
        }
    }
}
</script>

<style>
    .list-item {
        color: black;
        margin: 27px 24px;
        padding: 20px;
        background-color: white;
        border-radius: 5px;
        border: 1px solid #DFE3E8;
        box-sizing: border-box;
        cursor: pointer;
        transition: all ease 0.25s;
        width: 50%;
    }

    .list-item:hover {
        transform: scale(1.1, 1.1);
    }

    .list-item__user {
        font-weight: bold;
    }
</style>