<template>
  <div class="tab results-tab">
    <div class="content">
      <button id="download" class="btn btn-sm btn-success">
        <a style="color: #FFF; padding-left:auto; padding-right:auto" :href="ScriptData" :download="`Scenario_${Date.now()}.json`">Download</a>
      </button>
    </div>
    <div style="text-align: 'center">

    </div>
  </div>
</template>
<script>
  export default {
    name: 'ResultsTab',
    props: {
      code: { type: String, default: '' }
    },
    computed: {
      ScriptData(){
        return "data:text/plain;charset=UTF-8,"  + encodeURIComponent(this.code);
      }
    }
  }
</script>
<style lang="scss" scoped>
  @import "~styles/_variables.scss";

  .results-tab {
    .content {
      display:flex;
      flex-direction:column;
      height:100%;
      .generated-code {
        flex: 1;
        height:100%;
        overflow: auto;
        display: flex;
        flex-direction: column-reverse;
        max-height: $max-content-height;
      }

      pre {
        padding: 0 $spacer;
        font-size: 12px;
      }
      .code {
        font-family: Consolas, Monaco, monospace;
        padding: $spacer;
      }
    }
  }
</style>
