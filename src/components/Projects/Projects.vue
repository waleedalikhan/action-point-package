<script setup lang="ts">
import { ref } from 'vue'
// @ts-ignore
import Card from '../global/Card.vue'
// @ts-ignore
import ProjectRow from '../Projects/ProjectRow.vue'
import { IProjectRowProps } from '../../interfaces'

let projects = ref<IProjectRowProps[]>([
  {
    id: 1,
    date: '03.02.23',
    title: 'Project Title',
    desc: 'Bla bla descriere',
    isActive: false,
  },
  {
    id: 2,
    date: '03.02.23',
    title: 'Project Title',
    desc: 'Bla bla descriere',
    isActive: true,
  },
  {
    id: 3,
    date: '05.01.23',
    title: 'Project Title',
    desc: 'Bla bla descriere',
    isActive: false,
  },
  {
    id: 4,
    date: '10.12.22',
    title: 'Project Title',
    desc: 'Bla bla descriere',
    isActive: false,
  },
  {
    id: 5,
    date: '04.11.22',
    title: 'Project Title',
    desc: 'Bla bla descriere',
    isActive: false,
  },
])

const updateProjects = (index: number) => {
  let updatedProjects: IProjectRowProps[] = [...projects.value]
  updatedProjects.forEach(
    (project: IProjectRowProps) => (project.isActive = false),
  )
  updatedProjects[index].isActive = true
  projects.value = updatedProjects
}
</script>

<template>
  <div>
    <div class="w-full pt-[10px] mb-5 pl-5">
      <h2 class="text-[21px] text-title font-poppins font-bold">Projects</h2>
    </div>
    <div class="w-full">
      <Card class="h-full">
        <div class="flex flex-wrap">
          <div
            v-for="(project, index) in projects"
            class="w-full mb-5"
            :key="project.id"
          >
            <ProjectRow
              :date="project.date"
              :title="project.title"
              :desc="project.desc"
              :isActive="project.isActive"
              :onRowClick="() => updateProjects(index)"
            />
          </div>
        </div>
      </Card>
    </div>
  </div>
</template>
