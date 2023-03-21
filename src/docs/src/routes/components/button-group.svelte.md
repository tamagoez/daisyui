---
title: Button group
desc: Button group shows buttons next to each other.
published: true
---

<script>
  import Component from "@components/Component.svelte"
  import ClassTable from "@components/ClassTable.svelte"
  import { prefix } from '$lib/stores';
  import { replace } from '$lib/actions';
</script>

<ClassTable
data="{[
  { type:'component', class: 'btn-group', desc: 'Container for grouping multiple buttons' },
  { type:'responsive', class: 'btn-group-horizontal', desc: 'Show buttons horizontally (default)' },
  { type:'responsive', class: 'btn-group-vertical', desc: 'Show buttons vertically' },
]}"
/>

<Component title="Button group">
<div class="btn-group">
  <button class="btn btn-active">Button</button>
  <button class="btn">Button</button>
  <button class="btn">Button</button>
</div>
<pre slot="html" use:replace={{ to: $prefix }}>{
`<div class="$$btn-group">
  <button class="$$btn $$btn-active">Button</button>
  <button class="$$btn">Button</button>
  <button class="$$btn">Button</button>
</div>`
}</pre>
<pre slot="react" use:replace={{ to: $prefix }}>{
`<div className="$$btn-group">
  <button className="$$btn $$btn-active">Button</button>
  <button className="$$btn">Button</button>
  <button className="$$btn">Button</button>
</div>`
}</pre>
</Component>

<Component title="Button group vertical">
<div class="btn-group btn-group-vertical">
  <button class="btn btn-active">Button</button>
  <button class="btn">Button</button>
  <button class="btn">Button</button>
</div>
<pre slot="html" use:replace={{ to: $prefix }}>{
`<div class="$$btn-group btn-group-vertical">
  <button class="$$btn $$btn-active">Button</button>
  <button class="$$btn">Button</button>
  <button class="$$btn">Button</button>
</div>`
}</pre>
<pre slot="react" use:replace={{ to: $prefix }}>{
`<div className="$$btn-group btn-group-vertical">
  <button className="$$btn $$btn-active">Button</button>
  <button className="$$btn">Button</button>
  <button className="$$btn">Button</button>
</div>`
}</pre>
</Component>

<Component title="Responsive - Vertical for small screen, Horizontal on large screen">
<div class="btn-group btn-group-vertical lg:btn-group-horizontal">
  <button class="btn btn-active">Button</button>
  <button class="btn">Button</button>
  <button class="btn">Button</button>
</div>
<pre slot="html" use:replace={{ to: $prefix }}>{
`<div class="$$btn-group btn-group-vertical lg:btn-group-horizontal">
  <button class="$$btn $$btn-active">Button</button>
  <button class="$$btn">Button</button>
  <button class="$$btn">Button</button>
</div>`
}</pre>
<pre slot="react" use:replace={{ to: $prefix }}>{
`<div className="$$btn-group $$btn-group-vertical lg:$$btn-group-horizontal">
  <button className="$$btn $$btn-active">Button</button>
  <button className="$$btn">Button</button>
  <button className="$$btn">Button</button>
</div>`
}</pre>
</Component>

<Component title="Button group with radio buttons">
<div class="btn-group">
  <input type="radio" name="options" data-title="1" class="btn" />
  <input type="radio" name="options" data-title="2" checked="checked" class="btn" />
  <input type="radio" name="options" data-title="3" class="btn" />
  <input type="radio" name="options" data-title="4" class="btn" />
</div>
<pre slot="html" use:replace={{ to: $prefix }}>{
`<div class="$$btn-group">
  <input type="radio" name="options" data-title="1" class="$$btn" />
  <input type="radio" name="options" data-title="2" class="$$btn" checked />
  <input type="radio" name="options" data-title="3" class="$$btn" />
  <input type="radio" name="options" data-title="4" class="$$btn" />
</div>`
}</pre>
<pre slot="react" use:replace={{ to: $prefix }}>{
`<div className="$$btn-group">
  <input type="radio" name="options" data-title="1" className="$$btn" />
  <input type="radio" name="options" data-title="2" className="$$btn" checked />
  <input type="radio" name="options" data-title="3" className="$$btn" />
  <input type="radio" name="options" data-title="4" className="$$btn" />
</div>`
}</pre>
</Component>
