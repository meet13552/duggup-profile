<script lang="ts">
    import { Button } from "./ui/button";

    import { onMount } from 'svelte';

    interface Props {
    jsonData: any;
  }

  export let jsonData: Props['jsonData'];
  
    let isFollowed = false;
    let buttonText = isFollowed ? 'Followed' : 'Follow';
    let dropShadow = isFollowed ? 'drop-shadow-[0_2px_#4D4D4D]' : 'drop-shadow-[0_4px_#4D4D4D]';

    function handleClick() {
        isFollowed = !isFollowed;
        buttonText = isFollowed ? 'Followed' : 'Follow';
        dropShadow = isFollowed ? 'drop-shadow-[0_2px_#4D4D4D]' : 'drop-shadow-[0_4px_#4D4D4D]';
    }
</script>


<div class="flex flex-row mx-[16%] mt-10 mb-4">
    <div class="flex flex-col flex-none">
        <img src="profile-image.jpeg" alt="" class="rounded-full w-[120px] h-[120px] border-[#EAEFF5] border-[5px] mb-2" />
        <p class="font-[700] text-[24px] text-[#4B5C6D] text-center leading-[24px]">{jsonData.profile_details.first_name}</p>
        <p class="font-[700] text-[24px] text-[#4B5C6D] text-center leading-[24px]">{jsonData.profile_details.last_name}</p>
    </div>

    <div class="flex flex-col mx-[6%] justify-center">
        <p class="font-[400] text-[14px] text-[#141618] text-left leading-[24px]">{jsonData.profile_details.bio}</p>

        <Button on:click={handleClick} variant="outline" class={"mt-[30px] font-[400] text-[14px] text-[#4D4D4D] w-[91px] h-[36px] border-[#4D4D4D] w-24 hover:bg-[#0066FF] hover:text-[#ffffff] hover:drop-shadow-[0_2px_#003A91] " + dropShadow}>
            {buttonText}
        </Button>
    </div>

    <div class="flex flex-col flex-none items-end mt-[20px]">
        <img src="logo.png" alt="" class="object-cover rounded-full w-[36px] h-[36px]"/>
        <p class="font-[700] text-[16px] text-[#000000]">{jsonData.profile_details.company}</p>
        <p class="font-[400] text-[12px] text-[#7A9299]">{jsonData.profile_details.current_position}</p>

        <div class="flex flex-row mt-4">
            <a href="{jsonData.profile_details.website}">
            <Button variant="link" class="text-[#4D4D4D] text-[14px] font-[400]">
                My Website
                <img src="icons/my-website.svg" alt="" class="ml-1"/>
            </Button>
            </a>

            <img src="icons/options.svg" alt="" />

        </div>
    </div>
</div>