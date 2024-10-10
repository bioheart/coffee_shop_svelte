<script>
    import { page } from '$app/stores';
    const menus = [{
            title:'Home',
            url:'/'
        },
        {
            title:'About',
            url:'/about'
        },
        {
            title:'Contact',
            url:'/contact'
        }
    ]
</script>
<nav class="flex flex-row w-full">
    <div class="w-5/12"><a href="/">LOGO</a></div>
    <ul class="flex flex-row w-6/12">
        {#each menus as item}
            <li class="mx-auto">
                <a href={item.url} class='text-orange-300 hover:text-orange-600 {item.url===$page.url?.pathname?'active':''}'>{item.title}</a>
            </li>
        {/each}
    </ul>
    <div class="social-icons">
        <a href="https://instagram.com">IG</a>
    </div>
</nav>

<style>
    .active {
        @apply text-orange-900; /* Change the background color and text color */
    }
    .social-icons {
        @apply flex w-1/12 mx-auto w-5;
    }
</style>