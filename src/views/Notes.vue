<template>
    <div class="notes">
        ici les notes
        <NotesComponent/>
    </div>
</template>

<script>
import NotesComponent from '@/components/NotesComponent.vue'

export default {
  name: 'Notes',
  components: {
    NotesComponent
  }
}
</script>
