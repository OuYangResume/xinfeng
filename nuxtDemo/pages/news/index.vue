<template>
  <div>
      <h2>News Index page</h2>
      <h2>{{$route.params.newsId}}</h2>
       <ul>
        <li><a href="/">Home</a></li>
        <li><a href="./news/123">News-123</a></li>
        <li><a href="./news/456">News-456</a></li>
        <li>
            <nuxt-link :to="{name: 'news-id', params: {id: 123, title: 'youngyangNuxt'}}">Nuxt</nuxt-link>
        </li>
        <li>
            <nuxt-link :to="{name: 'news-id', params: {id: 456, title: 'youngyangVUE'}}">VUE</nuxt-link>
        </li>
      </ul>
  </div>
</template>