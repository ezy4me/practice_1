<template>
  <q-page class="my-page q-py-md">
    <q-scroll-area class="col my-scroll">
      <q-timeline :layout="layout" color="secondary" class="q-pa-md bg-grey-10 rounded-borders">
        <q-timeline-entry heading class="text-center">
          DevPortfolio
        </q-timeline-entry>

        <q-timeline-entry icon="start" side="left" color="indigo-14">
          <template v-slot:title> Регистрация 📝 </template>
          <template v-slot:subtitle> Шаг 1 </template>

          <div>
            Создайте учетную запись и присоединяйтесь к нашему сообществу
            разработчиков. Заполните несколько полей и начните демонстрировать
            свои проекты.
          </div>
        </q-timeline-entry>

        <q-timeline-entry icon="input" side="right" color="indigo-14">
          <template v-slot:title> Авторизация 🔐 </template>
          <template v-slot:subtitle> Шаг 2 </template>
          <div>
            Войдите в свой аккаунт, чтобы получить доступ к вашему портфолио,
            управлять проектами и взаимодействовать с другими разработчиками.
          </div>
        </q-timeline-entry>
        <q-timeline-entry icon="add" side="left" color="indigo-14">
          <template v-slot:title> Добавление Проекта 🚀 </template>
          <template v-slot:subtitle> Шаг 3 </template>

          <div>
            Загружайте и описывайте свои проекты. Дайте каждому проекту
            название, добавьте описание и демонстрируйте свои навыки и
            достижения.
          </div>
        </q-timeline-entry>

        <q-timeline-entry icon="people" side="right" color="indigo-14">
          <template v-slot:title> Просмотр Портфолио 🖥️</template>
          <template v-slot:subtitle> Шаг 4 </template>

          <div>
            Исследуйте портфолио других разработчиков. Получайте вдохновение,
            изучайте новые подходы и находите единомышленников.
          </div>
        </q-timeline-entry>

        <q-timeline-entry color="orange" icon="message" side="left" >
          <template v-slot:title> Обратная Связь 💬 </template>
          <template v-slot:subtitle> Шаг 5 </template>

          <div>
            Делитесь своими мыслями и комментариями о проектах других
            разработчиков. Взаимодействуйте и помогайте друг другу расти
            профессионально.
          </div>
        </q-timeline-entry>
      </q-timeline>
    </q-scroll-area>
  </q-page>
</template>
<script>
import { useQuasar } from 'quasar'
import { computed } from 'vue'

export default {
  setup () {
    const $q = useQuasar()

    return {
      layout: computed(() => {
        return $q.screen.lt.sm ? 'dense' : ($q.screen.lt.md ? 'comfortable' : 'loose')
      })
    }
  }
}
</script>
<style lang=""></style>
