<script lang="ts">
	import CompanyOfficerCard from '$lib/components/ticker/CompanyOfficerCard.svelte';
	export let data: any;
	export let companyOfficers: any;
</script>

{#if data.ticker_info.companyOfficers}
	<div id="company-officers">
		<div class="flex items-center gap-2">
			<div class="text-3xl font-semibold">Company Officers</div>
			<!-- <OfficersIcon class="text-primary h-10 w-10" /> -->
		</div>
		<div class="flex w-full snap-x snap-mandatory gap-2 overflow-auto py-5">
			{#each companyOfficers as officer}
				<CompanyOfficerCard companyOfficers={officer} />
			{/each}
		</div>
	</div>
{/if}
