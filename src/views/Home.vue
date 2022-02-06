<script lang="ts">
  import Vue, { VNode, CreateElement } from "vue";

  export default Vue.extend({
    render(h: CreateElement): VNode {
      return h("h1", "Homepage");
    }
  });
</script>
