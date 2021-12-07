<template>
    <section>
        <h2>Name: {{ username }}</h2> <!-- variables in vue directives without data properties --> 
        <h3>Age: {{ userage }}</h3> <!-- won't be undefined if props are passed to the default function -->
    </section>
</template>

<script>
export default {
    props: [
        'username',
        'userage'
    ]
}
</script>
