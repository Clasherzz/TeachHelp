<script lang="ts">
    import '../../app.css';
    let keyPoints = [{ question: '', point: '' }];
    let fileNames: string[] = [];
  
    const addKeyPoint = () => {
      keyPoints = [...keyPoints, { question: '', point: '' }];
    };
  
    const handleFileUpload = (event: Event) => {
      const input = event.target as HTMLInputElement;
      if (input.files) {
        const files = Array.from(input.files);
        fileNames = files
          .filter(file => file.type === 'image/png')
          .map(file => file.name);
        console.log('Uploaded file names:', fileNames);
      }
    };
  
    const saveKeyPoints = () => {
      // Placeholder function to handle saving key points
      console.log('Saving key points:', keyPoints);
    };
  </script>
  
  <style>
    /* Add specific component styles if necessary */
  </style>
  
  <div class="container mx-auto p-6">
    <h2 class="text-3xl font-semibold mb-6 text-gray-800">Manage Key Points for Questions</h2>
    
    {#each keyPoints as keyPoint, index}
      <div class="mb-6 p-6 border border-gray-300 rounded-lg shadow-lg bg-white">
        <input
          type="text"
          bind:value={keyPoint.question}
          placeholder={`Question ${index + 1}`}
          class="border border-gray-300 rounded-lg p-3 w-full mb-4 focus:outline-none focus:ring-2 focus:ring-blue-500"
        />
        <textarea
          bind:value={keyPoint.point}
          placeholder={`Key Points for Question ${index + 1}`}
          class="border border-gray-300 rounded-lg p-3 w-full h-24 resize-none focus:outline-none focus:ring-2 focus:ring-blue-500"
        ></textarea>
      </div>
    {/each}
  
    <button
      on:click={addKeyPoint}
      class="bg-green-500 text-white p-3 rounded-lg w-full mt-4 hover:bg-green-600 transition duration-200"
    >
      Add Another Key Point
    </button>
  
    <button
      on:click={saveKeyPoints}
      class="bg-indigo-500 text-white p-3 rounded-lg w-full mt-4 hover:bg-indigo-600 transition duration-200"
    >
      Save Key Points
    </button>
  
    <h2 class="text-3xl font-semibold mt-8 mb-6 text-gray-800">Upload PNG Files</h2>
    
    <input
      type="file"
      accept=".png"
      multiple
      on:change={handleFileUpload}
      class="border border-gray-300 rounded-lg p-3 w-full mb-4"
    />
  </div>
  