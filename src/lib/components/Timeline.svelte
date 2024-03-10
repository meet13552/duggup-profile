<script lang="ts">
  import { ChevronUp } from "lucide-svelte";

  interface Props {
    jsonData: any;
  }

  export let jsonData: Props['jsonData'];

</script>

<div class="mx-[20%]">

    {#each jsonData.timeline as item}

    <div class="border absolute border-dashed border-[#778FB1] h-[290px] border mt-2"></div>

    <div class="pt-8 flex flex-row">
        <p class="-ml-[100px] mt-[107px] text-[12px] font-[400] text-[#7A9299]">{item.story_time}</p>
        <div class="rounded-full absolute -ml-[7px] h-[16px] w-[16px] flex bg-white border-[3px] border-[#0066FF] mt-[108px]"></div>
        <div class="border-[0.5px] border-[#D0D5DD] rounded-[12px] bg-white w-[344px] h-[226px] flex flex-col ml-24">
            <img src="{item.story_image_1}" alt="" class="object-cover rounded-t-[12px] w-[344px] h-[136px]"/>
            <div class="flex flex-row justify-center items-center h-full">
            <p class="font-[400] text-[14px] text-[#141618] leading-[21px] mx-6">{item.story_1}</p>
            </div>
        </div>

        <div class="border-[0.5px] border-[#D0D5DD] rounded-[12px] bg-white w-[344px] h-[226px] flex flex-col ml-12">
            <img src="{item.story_image_2}" alt="" class="object-cover rounded-t-[12px] w-[344px] h-[136px]"/>
            <div class="flex flex-row justify-center items-center h-full">
            <p class="font-[400] text-[14px] text-[#141618] leading-[21px] mx-6">{item.story_2}</p>
            </div>
        </div>
    </div>

    <div class="-ml-[11px] mt-[26px]">
        <ChevronUp class="text-[#778FB1]"/>
    </div>

    <div class="border absolute border-dashed border-[#778FB1] h-[150px] border -mt-[8px]"></div>

    <div class="flex flex-row">
        <div class="flex flex-col flex-none -ml-[90px]">
            <img src="{item.company_image}" alt="" class="object-cover rounded-full w-[48px] h-[48px]"/>
            <p class="-ml-[95px] text-right text-[16px] font-[700] text-[#141618] max-w-[140px]">{item.company}</p>
            <p class="-ml-[95px] text-right text-[12px] font-[400] text-[#7A9299] max-w-[140px]">{item.location}</p>
            <p class="-ml-[95px] text-right text-[12px] font-[400] text-[#7A9299] max-w-[140px]">Joined</p>
            <p class="-ml-[95px] text-right text-[12px] font-[400] text-[#7A9299] max-w-[140px]">{item.joined}</p>
        </div>
        <div class="rounded-full absolute -ml-[13.5px] h-[28px] w-[28px] flex bg-white border-[9px] border-[#0066FF] mt-[40px]"></div>

        <div class="border-[0.5px] border-[#D0D5DD] rounded-[12px] bg-white w-[733px] h-[83px] flex flex-col ml-24 mt-3">

            <div class="flex flex-col justify-center h-full">
                <p class="font-[700] text-[20px] text-[#141618] mx-6">Co-Founder & CEO</p>
                <p class="font-[400] text-[12px] text-[#7A9299] mx-6">Full-time · Remote</p>
            </div>

        </div>
    </div>

{/each}
</div>

  