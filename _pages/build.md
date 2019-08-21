---
permalink: /build/
layout: single
title: "Build"
excerpt: "Build"
last_modified_at:
---

<script src="/assets/google-blockly/blockly_compressed.js"></script>
<script src="/assets/google-blockly/blocks_compressed.js"></script>
<script src="/assets/google-blockly/msg/js/en.js"></script>

<div id="blocklyDiv" style="position: absolute"></div>

<script>
  var blocklyArea = document.getElementById('blocklyArea');
  var blocklyDiv = document.getElementById('blocklyDiv');
  var workspace = Blockly.inject(blocklyDiv,
      {toolbox: document.getElementById('toolbox')});
  var onresize = function(e) {
    // Compute the absolute coordinates and dimensions of blocklyArea.
    var element = blocklyArea;
    var x = 0;
    var y = 0;
    do {
      x += element.offsetLeft;
      y += element.offsetTop;
      element = element.offsetParent;
    } while (element);
    // Position blocklyDiv over blocklyArea.
    blocklyDiv.style.left = x + 'px';
    blocklyDiv.style.top = y + 'px';
    blocklyDiv.style.width = blocklyArea.offsetWidth + 'px';
    blocklyDiv.style.height = blocklyArea.offsetHeight + 'px';
    Blockly.svgResize(workspace);
  };
  window.addEventListener('resize', onresize, false);
  onresize();
  Blockly.svgResize(workspace);
</script>

<dive id="blocklyArea">
</dive>
