<!-- @NewPost.component.vue -->
<!-- ⚫️⚫️☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰ -->

// 🌀🌀💻 SCRIPT 💻🌀🌀
<script setup lang="ts">
// 🌀🌀💻 ☰☰☰☰ imports ☰☰☰☰ 💻🌀🌀
import PostWriterComponent from '@/components/post-writer/PostWriter.component.vue'
import { PostType } from "@/types/Post.type"
import moment from "moment"
// ⚫️⚫️☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰
/**
* One drawback of the type-only defineProps declaration is that it doesn't
 * have a way to provide default values for the props. To resolve this problem,
 * a withDefaults compiler macro is also provided:
 * ☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰
 *  const props = withDefaults(defineProps<PostType>(), {
    created: moment,
 	  id: "-1",
    title: "Enter your title..."
    })
*/
// 🌀🌀💻 ☰☰☰☰☰☰☰☰☰☰☰ setup ☰☰☰☰☰☰☰☰☰☰☰ 💻🌀🌀
const newPost: PostType = {
	created: moment(),
	id: "-1",
	title: "Enter your title..."
}

const savePost = (post: PostType) => {
	//..........
	console.log('savePost emit:', post)
}
</script>
<!-- ⚫️⚫️☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰ -->

// 🌀🌀💻 HTML 💻🌀🌀
<template>
  <!-- 🎵🎵🔲🔲◾☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰ -->

  <!--☰☰☰☰| New-Post |☰☰☰☰-->
	<PostWriterComponent
		:post="newPost"
		@savePost="savePost"
	/>

  <!-- 🎵🎵🔲🔲◾☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰ -->
</template>
<!-- ⚫️⚫️☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰ -->

// 🌀🌀💻 STYLES 💻🌀🌀
<style lang="scss">

</style>
<!-- ⚫️⚫️☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰ -->
