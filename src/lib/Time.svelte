<script lang="ts">
	export let dateString: string;
	const date = new Date(dateString);
	const hours = date.getHours();
	const minutes = date.getMinutes() < 10 ? `0${date.getMinutes()}` : `${date.getMinutes()}`;
	const formattedTime = `${hours}:${minutes}`;
</script>

<div>
	<p>{formattedTime}</p>
</div>
