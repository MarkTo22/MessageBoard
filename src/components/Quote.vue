<template>
    <div class="col-sm-6 col-md-4 col-lg-3">
        <div class="panel panel-default">
            <div class="panel-body quote">
                <slot></slot>
            </div>
        </div>        
    </div>
</template>


<script>
    export default{
     
    }
</script>

<style lang="scss">
    .panel-body{
        font-size: 20px;
        color:#666;
    }

    .quote{
        border:1px solid red;
        cursor:pointer
    }
</style>