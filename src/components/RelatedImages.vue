<template>
  <div class="photo_related-images">
    <h3 class="b-header">
      {{ $t('photo-details.related-images') }}
    </h3>
    <SearchGridManualLoad
      v-if="isPrimaryImageLoaded === true"
      :images-count="imagesCount"
      :images="relatedImages"
      :query="query"
      :filter="filter"
      :include-analytics="false"
      :use-infinite-scroll="false"
      :include-add-to-list="false"
    />
  </div>
</template>

<script>
export default {
  name: 'RelatedImages',
  props: [
    'relatedImages',
    'imagesCount',
    'query',
    'filter',
    'isPrimaryImageLoaded',
  ],
}
</script>
