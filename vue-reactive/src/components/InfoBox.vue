<template>
    <div class="infobox w-[45vw] h-[40vw] bg-teal-100 rounded-xl border-6 shadow-xl">
      
      <header class="bg-blue-600 text-white py-8">
        <div class="container mx-auto text-center">
            <h1 class="text-4xl font-bold">16 Personalities</h1>
            <p class="text-lg mt-2">Discover Your Personality Type Based on Myers-Briggs Theory</p>
        </div>
      </header>

    <section class="container mx-auto my-12 px-6">
        <div class="bg-white rounded-lg shadow-lg p-6 mb-8">
            <h2 class="text-3xl font-bold mb-4">What is 16 Personalities?</h2>
            <p class="text-lg leading-relaxed">
                <strong>16 Personalities</strong> is a popular online platform that offers a free personality test based on the
                <strong>Myers-Briggs Type Indicator (MBTI)</strong>, a well-known psychological framework for understanding
                personality differences. The website helps you discover your unique personality type, understand your
                strengths and weaknesses, and how to apply this knowledge to various aspects of your life.
            </p>
        </div>

        <div class="bg-white rounded-lg shadow-lg p-6 mb-8">
            <h2 class="text-3xl font-bold mb-4">The 16 Personality Types</h2>
            <p class="text-lg leading-relaxed mb-4">
                The 16 personality types are divided into four categories based on the following traits:
            </p>
            <div class="grid grid-cols-2 gap-6 md:grid-cols-4">
                <div class="bg-purple-100 p-4 rounded-lg text-center">
                    <h3 class="text-xl font-semibold">Analysts</h3>
                    <p class="text-sm">Logical, strategic thinkers (e.g., INTJ, INTP, ENTJ, ENTP)</p>
                </div>
                <div class="bg-green-100 p-4 rounded-lg text-center">
                    <h3 class="text-xl font-semibold">Diplomats</h3>
                    <p class="text-sm">Empathetic, idealistic individuals (e.g., INFJ, INFP, ENFJ, ENFP)</p>
                </div>
                <div class="bg-blue-100 p-4 rounded-lg text-center">
                    <h3 class="text-xl font-semibold">Sentinels</h3>
                    <p class="text-sm">Practical and dependable personalities (e.g., ISTJ, ISFJ, ESTJ, ESFJ)</p>
                </div>
                <div class="bg-yellow-100 p-4 rounded-lg text-center">
                    <h3 class="text-xl font-semibold">Explorers</h3>
                    <p class="text-sm">Spontaneous and adaptable individuals (e.g., ISTP, ISFP, ESTP, ESFP)</p>
                </div>
            </div>
        </div>

        
        <div class="bg-white rounded-lg shadow-lg p-6 mb-8">
            <h2 class="text-3xl font-bold mb-4">Why Use 16 Personalities?</h2>
            <ul class="list-disc pl-6 space-y-4 text-lg leading-relaxed">
                <li><strong>Self-Awareness:</strong> Understand your strengths, challenges, and tendencies.</li>
                <li><strong>Career Guidance:</strong> Receive advice on career paths that align with your personality type.</li>
                <li><strong>Relationship Compatibility:</strong> Explore how you interact with others based on personality types.</li>
                <li><strong>Free to Use:</strong> The test is completely free with additional premium insights available.</li>
            </ul>
        </div>

        <div class="bg-white rounded-lg shadow-lg p-6 mb-8">
            <h2 class="text-3xl font-bold mb-4">Purpose of this Website</h2>
            <p class="text-lg leading-relaxed">
                This website is just a gallery of the personality types, with the ability to set one as one's profile.
                It is not in any way connected to the website, it is a one-off creation taking inspiration from 16 Personalities.
                To use this site, each section on the circle refers to one of the four categories which each contain four personalities themselves.
                The goal of this site is to allow exploration and the creation of fun profiles. To find more information, visit the actual 16 Personalities site.
            </p>
        </div>
        
        <div class="bg-white rounded-lg shadow-lg p-6 mb-8">
            <h2 class="text-3xl font-bold mb-4">How to Take the Test</h2>
            <p class="text-lg leading-relaxed">
                Taking the test is simple! Just visit the website, answer a series of multiple-choice questions, and in
                just a few minutes, you'll receive your personality type, complete with a detailed description and actionable
                insights. The test is free and takes around 10-15 minutes to complete.
            </p>
        </div>
    </section>
    </div>
</template>

<script setup>

</script>

<style lang="css" scoped>

.infobox{
  border-color: rgb(0, 146, 146);
  overflow-y: scroll;
  scrollbar-width: none;
}
.text{
  font-size: 64px;
}

</style>