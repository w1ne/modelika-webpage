---
permalink: /build/
layout: splash
author_profile: false
classes: wide
title: "Build"
excerpt: "Build"
last_modified_at:
---
<div id="blocklyArea"></div>
<div id="blocklyDiv" style="height: 800px; width: 100%;"></div>

<xml xmlns="https://developers.google.com/blockly/xml" id="toolbox" style="display: none">
    <block type="controls_if"></block>
    <block type="logic_compare"></block>
    <block type="controls_repeat_ext"></block>
    <block type="math_number">
      <field name="NUM">123</field>
    </block>
    <block type="math_arithmetic"></block>
    <block type="text"></block>
    <block type="text_print"></block>
</xml>

<script src="/assets/google-blockly/blockly_compressed.js"></script>
<script src="/assets/google-blockly/blocks_compressed.js"></script>
<script src="/assets/google-blockly/msg/js/en.js"></script>

<script>
  var workspace = Blockly.inject('blocklyDiv',
      {toolbox: document.getElementById('toolbox')});
</script>
