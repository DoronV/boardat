<template>
    <div class="courses">
        <h1>Courses</h1>
        <div class="course-list">
            <div v-for="course in courses.data" :key="course.id">
                <h2>{{ course.attributes.Name }}</h2>
                <p>{{ course.attributes.Description }}</p>
            </div>
        </div> 
        <div>test</div>
        <footer>
            <!-- Footer content here -->
        </footer>
    </div>
</template>

<script>
export default {
    name: 'CoursesView',
    data() {
        return {
            courses: [] // Store courses data here
        }
    },
    async mounted() {
        const response = await fetch('http://localhost:1337/api/courses');
        if (response.ok) {
            this.courses = await response.json();
            console.log('Courses:', this.courses);
        } else {
            console.error('Failed to fetch courses');
        }
    }
}
</script>

<style scoped>
.courses-view {
    /* Add styles for the courses view container */
}

.course-list {
    /* Add styles for the course list container */
}

footer {
    /* Add styles for the footer */
}
</style>
