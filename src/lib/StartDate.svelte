<script lang="ts">
	export let dateString: string;
	const date = new Date(dateString);
	const year = date.getFullYear();
	const month = date.getMonth() + 1;
	const day = date.getDate();
	const formattedDate = month + '/' + day + '/' + year;
</script>

<div>
	<p>{formattedDate}</p>
</div>
