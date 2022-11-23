<script setup>
import AppCard from "../components/AppCard.vue";
import AppLogo from "../components/AppLogo.vue";
import AppHeader from "../components/AppHeader.vue";
import AppFooter from "../components/TheFooter.vue";
import AppList from "../components/AppList.vue";

const info = {
  title: "Welcome to the Home Page",
  context: "This the home page for this project.",
};

const gmail = {
  text: "Gmail",
  src: "src/assets/images/gmail.svg",
  alt: "Gmail Logo",
};

const github = {
  text: "GitHub",
  src: "src/assets/images/github.svg",
  alt: "Github Logo",
};

const cardInfo = [
  {
    title: "First",
    text: "First Card",
  },
  {
    title: "Second",
    text: "Second Card",
  },
  {
    title: "Third",
    text: "Third Card",
  },
];

const listArray = [
  {
    text1: "Item one",
    text2: "Other item one",
  },
  {
    text1: "Item two",
    text2: "Other item two",
  },
  {
    text1: "Item three",
    text2: "Other item three",
  },
  {
    text1: "Item four",
    text2: "Other item four",
  },
];
</script>

<template>
  <main>
    <AppHeader
      :title="info.title"
      :context="info.context"
      color="text-blue-500"
    >
      <p class="text-xl text-red-500">This text added with slot</p>
    </AppHeader>
    <section class="flex items-center justify-center gap-4">
      <AppLogo
        :text="github.text"
        bgColor="bg-indigo-500"
        :src="github.src"
        :alt="github.alt"
      />
      <AppLogo
        text="Apple"
        bgColor="bg-red-500"
        src="src/assets/images/apple.svg"
        altText="Apple Logo"
      />
      <AppLogo
        :text="gmail.text"
        bgColor="bg-emerald-500"
        :src="gmail.src"
        :altText="gmail.alt"
      />
    </section>
    <section class="flex justify-center gap-4">
      <AppCard
        v-for="card in cardInfo"
        :key="card.id"
        :cardTitle="card.title"
        :cardText="card.text"
        :text="test"
      >
      </AppCard>
    </section>
    <section>
      <AppList :text="listArray" />
    </section>
  </main>
  <AppFooter />
</template>
