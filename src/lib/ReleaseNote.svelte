<script lang="ts">
  const message = 'Movable Type 8 来季秋にリリース予定！！！';
</script>

<!--Add this line to your web component-->
<svelte:options tag="release-note" />
<div class="release-note">
  <p>{message}</p>
</div>

<style>
.release-note {
  width: 100%;
  padding: 10px;
  box-sizing: border-box;
  background: #0176bf;
  color: #FFF;
}
.release-note p {
  margin: 0;
}
</style>
