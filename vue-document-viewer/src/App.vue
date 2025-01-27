<template>
  <div ref="viewer" style="position: absolute; left: 0; right: 0; top: 0; bottom: 0"></div>
</template>
<script>
  import 'devexpress-reporting/dx-webdocumentviewer';
  import {DxReportViewer} from 'devexpress-reporting/dx-webdocumentviewer';
  import * as ko from 'knockout';

  export default {
    name: "WebDocumentViewer",
    mounted() {
      const reportUrl = ko.observable("TestReport");
      const viewerRef = this.$refs.viewer;
      const requestOptions = {
        host: " http://localhost:5000/",
        invokeAction: "DXXRDV"
      };
      const viewer = new DxReportViewer(viewerRef, {
        reportUrl,
        requestOptions
      });
      viewer.render();
    },
    beforeUnmount() {
      ko.cleanNode(this.$refs.viewer);
    }
  };
</script>