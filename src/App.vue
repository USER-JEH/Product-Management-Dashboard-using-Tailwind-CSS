<script setup>
import OverviewIcon from "./icons/overview.svg";
import ShoppingBagIcon from "./icons/shopping-bag.svg";
import GraphIcon from "./icons/graph.svg";
import CalendarIcon from "./icons/calendar.svg";
import WalletIcon from "./icons/wallet.svg";
import FileIcon from "./icons/file.svg";
import ChatIcon from "./icons/chat.svg";
import GroupChatIcon from "./icons/group-chat.svg";
import SettingsIcon from "./icons/settings.svg";
import LogoutIcon from "./icons/logout.svg";

const sidebar =[
   [
    { name: "Overview", icon: OverviewIcon },
    { name: "Products", icon: ShoppingBagIcon },
    { name: "Analytics", icon: GraphIcon },
    { name: "Schedule", icon: CalendarIcon },
    { name: "Payout", icon: WalletIcon },
    { name: "Statements", icon: FileIcon },
  ],
  [
    { name: "Help", icon: ChatIcon },
    { name: "Community", icon: GroupChatIcon },
    { name: "Settings", icon: SettingsIcon },
    { name: "Logout", icon: LogoutIcon },
  ],
]
</script>


<template>
  <div class="w-full min-h-screen font-sans text-gray-900 bg-gray-50">
    <aside class="py-6 px-10 w-64 border-r border-gray-200">
      <img src="../public/img/logo.png" alt="" class="w-28" />
      <ul v-for="group in sidebar" class="flex flex-col gap-y-6 pt-20 font-extrabold">
        <li v-for="item in group">
          <a href="#" class="flex gap-x-4 items-start py-2 text-gray-500 hover:text-indigo-600">    
            <component :is="item.icon" class="w-6 h-6 fill-current"></component>
            <span>{{item.name}}</span>
          </a>
        </li>
      </ul>
    </aside>
  </div>
</template>