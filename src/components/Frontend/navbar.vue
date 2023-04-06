<script setup>
    const themes = [
        'light',
        'dark',
        'cupcake',
        'bumblebee',
        'emerald',
        'corporate',
        'synthwave',
        'retro',
        'cyberpunk',
        'valentine',
        'halloween',
        'garden',
        'forest',
        'aqua',
        'lofi',
        'pastel',
        'fantasy',
        'wireframe',
        'black',
        'luxury',
        'dracula',
        'cmyk',
        'autumn',
        'business',
        'acid',
        'lemonade',
        'night',
        'coffee',
        'winter',
    ];
</script>
<template>
    <div className="navbar top-0 index-0">
        <div className="navbar-start">
            <div className="dropdown">
                <label tabIndex={0} className="btn btn-ghost lg:hidden">
                    <svg width="20" height="20" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" class="inline-block h-5 w-5 stroke-current md:h-6 md:w-6"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path></svg>
                </label>
                <ul tabIndex={0}
                    className="menu menu-compact dropdown-content mt-3 p-2 shadow bg-base-100 rounded-box w-52">
                    <li><a>Item 1</a></li>
                    <li tabIndex={0}>
                        <a className="justify-between">
                            Parent
                            <svg className="fill-current" xmlns="http://www.w3.org/2000/svg" width="24" height="24"
                                viewBox="0 0 24 24">
                                <path d="M8.59,16.58L13.17,12L8.59,7.41L10,6L16,12L10,18L8.59,16.58Z" />
                            </svg>
                        </a>
                        <ul className="p-2">
                            <li><a>Submenu 1</a></li>
                            <li><a>Submenu 2</a></li>
                        </ul>
                    </li>
                    <li><a>Item 3</a></li>
                </ul>
            </div>
            <a className="btn btn-ghost normal-case text-xl">JUdul</a>
        </div>
        <div className="navbar-center hidden lg:flex">
            <ul className="menu menu-horizontal px-1">
                <li><a>Item 1</a></li>
                <li tabIndex={0}>
                    <a>
                        Parent
                        <svg className="fill-current" xmlns="http://www.w3.org/2000/svg" width="20" height="20"
                            viewBox="0 0 24 24">
                            <path d="M7.41,8.58L12,13.17L16.59,8.58L18,10L12,16L6,10L7.41,8.58Z" />
                        </svg>
                    </a>
                    <ul className="p-2">
                        <li><a>Submenu 1</a></li>
                        <li><a>Submenu 2</a></li>
                    </ul>
                </li>
                <li><a>Item 3</a></li>
            </ul>
        </div>
        <div className="navbar-end lg:flex sm:flex">
            <div id="theme-switch" title="Ganti Tema" class="dropdown dropdown-end">
                <div tabindex="0" class="btn gap-1 normal-case btn-ghost">
                    <svg width="20" height="20" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                        class="inline-block h-5 w-5 stroke-current md:h-6 md:w-6">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M7 21a4 4 0 01-4-4V5a2 2 0 012-2h4a2 2 0 012 2v12a4 4 0 01-4 4zm0 0h12a2 2 0 002-2v-4a2 2 0 00-2-2h-2.343M11 7.343l1.657-1.657a2 2 0 012.828 0l2.829 2.829a2 2 0 010 2.828l-8.486 8.485M7 17h.01">
                        </path>
                    </svg>
                    <span class="hidden md:inline">Tema</span>
                    <svg width="12px" height="12px" class="ml-1 hidden h-3 w-3 fill-current opacity-60 sm:inline-block"
                        xmlns="http://www.w3.org/2000/svg" viewBox="0 0 2048 2048">
                        <path d="M1799 349l242 241-1017 1017L7 590l242-241 775 775 775-775z"></path>
                    </svg>
                </div>
                <div
                    class="dropdown-content bg-base-200 text-base-content rounded-t-box rounded-b-box top-px max-h-96 h-[70vh] w-52 overflow-y-auto shadow-2xl mt-16">
                    <div class="grid grid-cols-1 gap-3 p-3" tabindex="0">
                        <button v-for="theme of themes"
                            class="outline-base-content overflow-hidden rounded-lg text-left"
                            :data-set-theme="[theme]" data-act-class="[&_svg]:visible" >
                            <div :data-theme="[theme]"
                                class="bg-base-100 text-base-content w-full cursor-pointer font-sans">
                                <div class="grid grid-cols-5 grid-rows-3">
                                    <div class="col-span-5 row-span-3 row-start-1 flex gap-2 py-3 px-4 items-center">
                                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16"
                                            viewBox="0 0 24 24" fill="currentColor" class="w-3 h-3 invisible">
                                            <path
                                                d="M20.285 2l-11.285 11.567-5.286-5.011-3.714 3.716 9 8.728 15-15.285z">
                                            </path>
                                        </svg>
                                        <div class="flex-grow text-sm font-bold">{{ theme }}</div>
                                        <div class="flex flex-shrink-0 flex-wrap gap-1 h-full">
                                            <div class="bg-primary w-2 rounded"></div>
                                            <div class="bg-secondary w-2 rounded"></div>
                                            <div class="bg-accent w-2 rounded"></div>
                                            <div class="bg-neutral w-2 rounded"></div>
                                        </div>
                                    </div>
                                </div>
                            </div>

                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>