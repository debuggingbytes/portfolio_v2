<template>
  <div class="resume">
    <div class="resume__modal">
      <!-- Helper buttons -->
      <div class="resume__links">
        <!-- <span class="alert alert-success">Email</span>
        <span class="alert alert-warn">Download</span>
        <span class="alert alert-success">Email</span> -->
      </div>
      <!-- Close Button -->
      <div class="resume__close">
        <a href='#resume' @click.prevent="this.$emit('event')">&cross;</a>
      </div>
      <!-- Resume -->
      <div class="resume__header">
        <h2 class="h3 mb-sm">Kris Cartmell</h2>
        <hr>
        <p class="content pt-sm">
          <span class="content-block">
            <span class="content-inline">Email:</span> kris@debuggingbytes.com
          </span>
          <span class="content-block">
            <span class="content-inline">Location:</span> Alberta, Canada
          </span>
          <span class="content-block">
            <span class="content-inline">Objective:</span> To obtain a position as a full stack developer within a company.
          </span>
        </p>
      </div>
      <div class="resume__body pt-md">
        <h3 class="h3">
          Work Experience
        </h3>
        <div class="flex space-between pt-sm">
          <div><span class="fw-lg">DebuggingBytes.com </span></div>
          <div>2010 - Current</div>
        </div>
      </div>
      <span class="content-block pt-xs">
        <span class="content-inline">Position:</span> Freelance Full Stack developer, Owner.
      </span>
      <div class="content-block pt-sm">
        <div class="content-inline">Responsibilities</div>
        <div class="pt-xs">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ducimus, deserunt eaque ex architecto deleniti, assumenda possimus rem commodi labore esse laboriosam atque odit reprehenderit, natus unde dolore! Eligendi, nulla ea reprehenderit earum saepe nostrum at unde nam accusamus qui, iure, beatae voluptate illum tenetur. Harum ipsum provident totam vel sapiente explicabo necessitatibus dignissimos, temporibus quae delectus laboriosam repellat possimus quidem quas? Ipsam maxime laudantium minima ipsum culpa assumenda id! Officiis error molestias odit natus tempore, magni tenetur placeat pariatur reprehenderit recusandae repellat, fugit quisquam. Dolores vero aut qui autem, quaerat reiciendis explicabo aliquid impedit similique magni labore quod repellendus fugiat.
        </div>
      </div>
      
    </div>
    
  </div>
</template>

<script>
export default {
  name: "ResumeLayout"

}
</script>

<style>

</style>