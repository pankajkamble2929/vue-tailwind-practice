<template>
    <div class="flex items-start">
      <ul class="nav nav-tabs flex flex-col flex-wrap list-none border-b-0 pl-0 mr-4" id="tabs-tabVertical" role="tablist">
        <li class="nav-item flex-grow text-center" role="presentation">
          <a href="#tabs-homeVertical" class="
            nav-link
            block
            font-medium
            text-xs
            leading-tight
            uppercase
            border-x-0 border-t-0 border-b-2 border-transparent
            px-6
            py-3
            my-2
            hover:border-transparent hover:bg-gray-100
            focus:border-transparent
            active
          " :class="{ 'active': activeTab === 'home' }" @click.prevent="activeTab = 'home'" id="tabs-home-tabVertical" role="tab" aria-controls="tabs-homeVertical" aria-selected="true">Home</a>
        </li>
        <li class="nav-item flex-grow text-center" role="presentation">
          <a href="#tabs-profileVertical" class="
            nav-link
            block
            font-medium
            text-xs
            leading-tight
            uppercase
            border-x-0 border-t-0 border-b-2 border-transparent
            px-6
            py-3
            my-2
            hover:border-transparent hover:bg-gray-100
            focus:border-transparent
          " :class="{ 'active': activeTab === 'profile' }" @click.prevent="activeTab = 'profile'" id="tabs-profile-tabVertical" role="tab" aria-controls="tabs-profileVertical" aria-selected="false">Profile</a>
        </li>
        <li class="nav-item flex-grow text-center" role="presentation">
          <a href="#tabs-messagesVertical" class="
            nav-link
            block
            font-medium
            text-xs
            leading-tight
            uppercase
            border-x-0 border-t-0 border-b-2 border-transparent
            px-6
            py-3
            my-2
            hover:border-transparent hover:bg-gray-100
            focus:border-transparent
          " :class="{ 'active': activeTab === 'messages' }" @click.prevent="activeTab = 'messages'" id="tabs-messages-tabVertical" role="tab" aria-controls="tabs-messagesVertical" aria-selected="false">Messages</a>
        </li>
      </ul>
      <div class="tab-content" id="tabs-tabContentVertical">
        <div class="tab-pane fade show active" :class="{ 'active': activeTab === 'home' }" id="tabs-homeVertical" role="tabpanel" aria-labelledby="tabs-home-tabVertical">
          Tab 1 content vertical
        </div>
        <div class="tab-pane fade" :class="{ 'active': activeTab === 'profile' }" id="tabs-profileVertical" role="tabpanel" aria-labelledby="tabs-profile-tabVertical">
          Tab 2 content vertical
        </div>
        <div class="tab-pane fade" :class="{ 'active': activeTab === 'messages' }" id="tabs-messagesVertical" role="tabpanel" aria-labelledby="tabs-profile-tabVertical">
          Tab 3 content vertical
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        activeTab: 'home'
      }
    }
  }
  </script>
  