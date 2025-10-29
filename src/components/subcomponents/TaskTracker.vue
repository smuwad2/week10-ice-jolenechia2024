<script>
    // TODO: Complete the code
    export default { 
        props:{
            task: Object,
            idx: Number
        },
        // Hint: insert properties task (Object) and idx (Number)
        emits: ['removeTask']

    }
</script>

<template>
    <div class="card" style="width: 18rem; display: inline-block">
        <div class="card-body">
            <h5 class="card-title">Deadline: {{task.deadline }}</h5>
            <hr></hr>
            <p class="card-text">{{ task.desc }}</p>
            <button class="btn btn-primary" @click="$emit('removeTask', idx)">Done</button>
        </div>
    </div>
</template>



