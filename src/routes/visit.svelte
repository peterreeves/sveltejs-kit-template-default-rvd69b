<script context="module">
	export const load = ({ url }) => {
		return {
			props: {
				id: url.searchParams.get("id"),
			}
		}
	};
</script>

<script>
  export let id;
  import { page } from "$app/stores";

  const helper = (newId) => {
    const searchParams = $page.url.searchParams;
    searchParams.set("id", newId);
    return "/visit?" + searchParams.toString();
  }
</script>

<section>
  <h1>Visit {id}</h1>
  <a href="{helper(1)}">Visit 1 ({helper(1)})</a>
  <a href="{helper(2)}">Visit 2 ({helper(2)})</a>
  <br>
  <br>
  <a href="/">Back to Homepage</a>
</section>

<style>
  section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

  h1 {
		width: 100%;
	}
</style>
