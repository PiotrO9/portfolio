<script setup lang="ts">
function handleMenuItemSelect(e: MouseEvent) {
    const targetElement = (e.target as HTMLElement).closest(".list-item");
    if (!targetElement) return;

    const menuItemsList = document.querySelectorAll(".list-item");
    menuItemsList.forEach((listItem) => listItem.classList.remove("selected"));

    targetElement.classList.add("selected");
}
</script>

<template>
    <nav>
        <menu>
            <ul>
                <li class="list-item selected" @click="handleMenuItemSelect">
                    <router-link to="/">
                        Home
                    </router-link>
                </li>
                <li class="list-item " @click="handleMenuItemSelect">
                    <router-link to="/skills">
                        Skills & Career
                    </router-link>
                </li>
                <li class="list-item" @click="handleMenuItemSelect">
                    <router-link to="/contact">
                        Contact
                    </router-link>
                </li>
                <div class="indicator"></div>
            </ul>
        </menu>
    </nav>
</template>

<style lang="scss" scoped>
nav {
    width: 100%;
    display: flex;
    justify-content: center;
    margin-top: 20px;
}

menu {
    backdrop-filter: blur(8px);
    -webkit-backdrop-filter: blur(8px);
    border-radius: 20px;
    padding: 10px;
}

ul {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 30px;
    position: relative;
    animation: gap .2s ease-in-out;

    @media (width > 1024px) {
        gap: 40px;
    }

    li,
    a {
        color: white;
        text-decoration: none;
    }

    li {
        font-family: var(--font-base);
        font-weight: 600;
        font-size: 16px;
        z-index: 1;

        @media (width > 1024px) {
            font-size: 24px;
        }

        &.selected {
            a {
                color: var(--color-lime-base);
            }
        }

        &:nth-child(1) {
            &.selected {
                ~.indicator {
                    transform: translateX(0px);
                }
            }
        }

        &:nth-child(2) {
            &.selected {
                ~.indicator {
                    transform: translateX(72px);
                    width: 140px;

                    @media (width > 1024px) {
                        transform: translateX(103px);
                        width: 200px;
                    }
                }
            }
        }

        &:nth-child(3) {
            &.selected {
                ~.indicator {
                    transform: translateX(217px);
                    width: 86px;

                    @media (width > 1024px) {
                        transform: translateX(316px);
                        width: 118px;
                    }
                }
            }
        }
    }

    .indicator {
        width: 65px;
        height: 30px;
        position: absolute;
        left: -10px;
        border-radius: 20px;
        background-color: hsla(158, 23%, 18%, .7);
        transition: all .2s ease-in-out;
        filter: blur(1px);

        @media (width > 1024px) {
            width: 90px;
            height: 45px;
            left: -12px;
        }
    }
}
</style>