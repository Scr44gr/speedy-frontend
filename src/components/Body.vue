<template>
  <div class="body--container">
      <c-flex class="server-sections">
          <slot></slot>
      </c-flex>
  </div>
</template>

<script>

export default {
}
</script>

<style>

.body--container {
    width: 100%;
    height: 80vh;
}

.server-sections{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin: 14px;
}

@media screen and (max-height: 700px) {
    .body--container {
        height: 75vh;
    }
}

</style>