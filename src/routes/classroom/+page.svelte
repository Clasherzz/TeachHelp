<!-- <script lang="ts">
//   import axios from 'axios';
  import '../../app.css';

  let className = '';
  let students = [{ name: '', questionPaper: '' }];

  const createClassroom = async () => {
    // try {
    //   await axios.post('http://localhost:5000/api/create-classroom', { className });
    //   alert('Classroom created!');
    // } catch (error) {
    //   alert('Error creating classroom');
    // }
  };

  const addStudent = () => {
    students = [...students, { name: '', questionPaper: '' }];
  };

  const saveStudents = async () => {
    // try {
    //   for (const student of students) {
    //     await axios.post('http://localhost:5000/api/add-student', {
    //       className,
    //       studentName: student.name,
    //       questionPaper: student.questionPaper,
    //     });
    //   }
    //   alert('Students and question papers added successfully!');
    // } catch (error) {
    //   alert('Error adding students');
    // }
  };
</script>

<style>
  /* Add specific component styles if necessary */
</style>

<div class="container mx-auto p-4">
  <h2 class="text-2xl font-bold mb-4">Create a Classroom</h2>
  <div class="mb-4">
    <input
      type="text"
      bind:value={className}
      placeholder="Classroom Name"
      class="border p-2 w-full"
    />
    <button
      on:click={createClassroom}
      class="bg-blue-500 text-white p-2 mt-2 w-full hover:bg-blue-700"
    >
      Create Classroom
    </button>
  </div>

  <h2 class="text-2xl font-bold mb-4">Add Students</h2>
  {#each students as student, index}
    <div class="mb-4">
      <input
        type="text"
        bind:value={student.name}
        placeholder={`Student Name ${index + 1}`}
        class="border p-2 w-full"
      />
      <textarea
        bind:value={student.questionPaper}
        placeholder={`Question Paper Text for Student ${index + 1}`}
        class="border p-2 w-full mt-2"
      ></textarea>
    </div>
  {/each}

  <button
    on:click={addStudent}
    class="bg-green-500 text-white p-2 mt-2 w-full hover:bg-green-700"
  >
    Add Another Student
  </button>

  <button
    on:click={saveStudents}
    class="bg-indigo-500 text-white p-2 mt-4 w-full hover:bg-indigo-700"
  >
    Save All Students
  </button>
</div> -->


<script lang="ts">
    import '../../app.css';
  
    let className = '';
    let students = [{ name: '', questionPaper: '' }];
  
    const createClassroom = async () => {
      // try {
      //   await axios.post('http://localhost:5000/api/create-classroom', { className });
      //   alert('Classroom created!');
      // } catch (error) {
      //   alert('Error creating classroom');
      // }
    };
  
    const addStudent = () => {
      students = [...students, { name: '', questionPaper: '' }];
    };
  
    const saveStudents = async () => {
      // try {
      //   for (const student of students) {
      //     await axios.post('http://localhost:5000/api/add-student', {
      //       className,
      //       studentName: student.name,
      //       questionPaper: student.questionPaper,
      //     });
      //   }
      //   alert('Students and question papers added successfully!');
      // } catch (error) {
      //   alert('Error adding students');
      // }
    };
  </script>
  
  <style>
    /* Add specific component styles if necessary */
  </style>
  
  <div class="container mx-auto p-6">
    <h2 class="text-3xl font-semibold mb-6 text-gray-800">Create a Classroom</h2>
    <div class="mb-6 p-6 border border-gray-300 rounded-lg shadow-lg bg-white">
      <input
        type="text"
        bind:value={className}
        placeholder="Enter Classroom Name"
        class="border border-gray-300 rounded-lg p-3 w-full mb-4 focus:outline-none focus:ring-2 focus:ring-blue-500"
      />
      <button
        on:click={createClassroom}
        class="bg-blue-500 text-white p-3 rounded-lg w-full hover:bg-blue-600 transition duration-200"
      >
        Create Classroom
      </button>
    </div>
  
    <h2 class="text-3xl font-semibold mb-6 text-gray-800">Add Students</h2>
    {#each students as student, index}
      <div class="mb-6 p-6 border border-gray-300 rounded-lg shadow-lg bg-white">
        <input
          type="text"
          bind:value={student.name}
          placeholder={`Student Name ${index + 1}`}
          class="border border-gray-300 rounded-lg p-3 w-full mb-4 focus:outline-none focus:ring-2 focus:ring-blue-500"
        />
        <textarea
          bind:value={student.questionPaper}
          placeholder={`Question Paper Text for Student ${index + 1}`}
          class="border border-gray-300 rounded-lg p-3 w-full h-24 resize-none focus:outline-none focus:ring-2 focus:ring-blue-500"
        ></textarea>
      </div>
    {/each}
  
    <button
      on:click={addStudent}
      class="bg-green-500 text-white p-3 rounded-lg w-full mt-4 hover:bg-green-600 transition duration-200"
    >
      Add Another Student
    </button>
  
    <button
      on:click={saveStudents}
      class="bg-indigo-500 text-white p-3 rounded-lg w-full mt-4 hover:bg-indigo-600 transition duration-200"
    >
      Save All Students
    </button>
  </div>
  
