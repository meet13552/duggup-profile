<script lang="ts">
  import { Button } from "./ui/button";
  import { SquarePlus, ChevronDown } from 'lucide-svelte';

  interface Props {
    jsonData: any;
  }

  export let jsonData: Props['jsonData'];

</script>
<div class="bg-[#FCFCFF] z-10 sticky top-0 left-0">
<header class="flex h-16 mx-[10%] pt-4 justify-between">
<div class=" flex flex-row pt-2">
    <img src="icons/header-logo.svg" alt=""/>
</div>
<div class="flex flex-row">
    <Button variant="ghost" class="gap-2 font-[400] text-[14px] text-[#4D4D4D] w-24">
    <img src="icons/home.svg" alt="" />
        Home
    </Button>
    <Button variant="ghost" class="gap-2 font-[400] text-[14px] text-[#4D4D4D] w-24">
    <img src="icons/explore.svg" alt="" />
        Explore
    </Button>
    <Button variant="ghost" class="gap-2 font-[400] text-[14px] text-[#4D4D4D] w-24">
    <img src="icons/learn.svg" alt="" />
        Learn
    </Button>
    <div class="flex flex-row pl-10">
        <Button variant="outline" class="gap-2 font-[400] text-[14px] text-[#4D4D4D] w-[102px] h-[36px] border-[#4D4D4D] drop-shadow-[0_4px_#4D4D4D] w-24 hover:bg-[#0066FF] hover:text-[#ffffff] hover:drop-shadow-[0_2px_#003A91]">
            <SquarePlus class="size-[14px]"/>
            Post
        </Button>
    </div>
    <div class="flex flex-row flex-none pl-10">
        <img src="profile-image.jpeg" alt="" class="rounded-full border-[#4D4D4D] border-[0.5px] w-[46px] h-[46px]" />
        <Button variant="link" class="text-[#4D4D4D] text-[20px] font-[500] pt-3">
            {jsonData.profile_details.first_name} {jsonData.profile_details.last_name}
            <ChevronDown class="pl-2"/>
        </Button>
    </div>
</div>
</header>
<div class="border-t border-dotted border-[#525C69] mx-28 my-4"></div>
</div>