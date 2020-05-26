<template>
  <div class="tab help-tab">
    <div class="content">
      <h4>User Journey Recording</h4>
      <ul>
        <li>To start recording hit <strong>Record</strong></li>
        <li>Hit <kbd>tab</kbd> after you finish typing in an <kbd>input</kbd> element.</li>
        <li>Click links, inputs and other elements.</li>
        <li>Wait for full page load on each navigation. The icon will switch from <img src="/images/icon_rec.png"> to
          <img src="/images/icon_wait.png">.</li>
        <li>Click <strong>Pause</strong> when you want to navigate without recording anything.
          Hit <strong>Resume</strong> to continue recording.</li>
      </ul>
    </div>
    <div class="help-footer text-muted">
      powered by
      <a href="https://checklyhq.com" target="_blank">
        <img src="/images/text_racoon_logo.svg" alt="">
      </a>
    </div>
  </div>
</template>
<script>
  export default {
    name: 'HelpTab'
  }
</script>
<style lang="scss" scoped>
  @import "~styles/_variables.scss";
  @import "~styles/_mixins.scss";
  @import "~styles/_utils.scss";


  .help-tab {
    .content {
      padding: $spacer;
      text-align: left;

      ul {
        padding-left: 1rem;
      }

      pre {
        background: #272822;
        color: white;
        font-family: monospace;
        padding: 1rem;
        border-radius: 4px;
      }
    }

    .help-footer {
      @include footer();
      font-weight: normal;
      justify-content: flex-end;
      img {
        margin-left: 8px;
        width: 80px;
        vertical-align: middle;
      }
    }
  }
</style>
