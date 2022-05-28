<script setup>
  const route = useRoute()
  const products = useState('products')
  const product = products.value.find(p => p.name === route.params.name)
</script>

<template>
  <div>
    <h1>Termék: {{ $route.params.name }}</h1>
    <dl>
      <dt>id</dt>
      <dd>{{ product.id }}</dd>
      <dt>name</dt>
      <dd>{{ product.name }}</dd>
      <dt>description</dt>
      <dd>{{ product.description }}</dd>
      <dt>picture</dt>
      <dd>{{ product.picture }}</dd>
      <dt>category</dt>
      <dd>{{ product.category }}</dd>
      <dt>price</dt>
      <dd>{{ product.price }}</dd>
      <dt>stock</dt>
      <dd>{{ product.stock }}</dd>
    </dl>
  </div>
</template>

<style scoped>
  dt {
    display: inline-block;
    width: 5rem;
  }
  dd {
    display: inline;
  }
  dd::after {
    content: '\a';
    white-space: pre;
  }
</style>
