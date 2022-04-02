<template>
  <footer class="footer--container">
      <c-flex class="footer-content">
          <slot></slot>
      </c-flex>
  </footer>
</template>

<script>

export default {
}
</script>

<style>

.footer--container {
    width: 100%;
    height: 100%;
    background-color: #32304E;
}

.footer-content{
    display: flex;
    flex-direction: row;
    margin: 14px;
    justify-content: flex-start;
    padding: 10px;

}

</style>