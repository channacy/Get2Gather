<script lang="ts">
  import {Select} from "bits-ui";
  import SingleCalendar from "../components/SingleCalendar.svelte";

  const meetingTypes = [
    { value: "Weekly", label: "Weekly" },
    { value: "Single", label: "Single" },
  ];
</script>
 
<div class="body place-content-center">
  <div class="time-section">
    <h1>1. Select Meeting Type and Day</h1>
    <div class="meeting-type-select">
      <Select.Root items={meetingTypes}>
        <Select.Trigger
            class="inline-flex h-input w-[296px] items-center rounded-9px border border-border-input bg-background px-[11px] text-sm transition-colors placeholder:text-foreground-alt/50  focus:outline-none focus:ring-2 focus:ring-foreground focus:ring-offset-2 focus:ring-offset-background"
            aria-label="Select a meeting type">
          <Select.Value placeholder="Select a meeting type"/>
        </Select.Trigger>

        <Select.Content
          class="w-full rounded-xl border border-muted bg-background px-1 py-3 shadow-popover outline-none"
          sideOffset={8}
        >
        {#each meetingTypes as meetingType}
          <Select.Item
            class="flex h-10 w-full select-none items-center rounded-button py-3 pl-5 pr-1.5 text-sm outline-none transition-all duration-75 data-[highlighted]:bg-muted"
            value={meetingType.value}
            label={meetingType.label}
          >
            {meetingType.label}
          </Select.Item>
        {/each}
      </Select.Content>
      <Select.Input name="selectedMeetingType" />
      </Select.Root>
    </div>
    <div class="calendar">
      <SingleCalendar />
    </div>
  </div>
  <div class="info-section">
    <h1>2. Add Meeting Information</h1>
  </div>
</div>


<style lang="postcss">
  :global(html) {
    background-color: theme(colors.gray.100);
  }

  .body {
    display: flex;
    flex-direction: row;

  }

  .time-section, .info-section {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
</style>