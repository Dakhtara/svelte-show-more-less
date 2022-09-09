<script lang="ts">
import ShowMore from "./lib/ShowMore.svelte";
</script>

<div class="container mx-auto">
  <div class="w-4/12 mx-auto mt-8">
    <div class="bg-white rounded flex flex-col px-4 py-2">
      <div class="mb-3">
        <span class="text-xl">Titre d'un article</span>
      </div>

        <ShowMore showMoreText="Voir plus" showLessText="Voir moins" >
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean ullamcorper, elit id euismod laoreet, nisi justo pulvinar dolor, vitae tincidunt nibh ligula vitae erat. Curabitur vel massa a massa blandit convallis cursus vitae diam. Duis at erat nunc. Aenean id augue lacus. Phasellus at convallis sem. Ut quis euismod leo, porttitor convallis libero. Maecenas leo lacus, tempus sed vestibulum ut, efficitur sit amet mi. Morbi sed libero vel lorem ullamcorper faucibus. Sed pulvinar dapibus est, vitae egestas metus ornare a.
Phasellus tincidunt hendrerit efficitur. Ut tempus diam fringilla eros tempor, euismod euismod mi fermentum. Pellentesque tempus erat quis felis ultricies, ut fringilla nisi facilisis. Proin rhoncus laoreet purus eu fringilla. Quisque egestas nisi non odio laoreet interdum. Cras sollicitudin dui massa, eu egestas nisl venenatis et. Aenean lorem urna, molestie ac urna eget, mattis dapibus enim. Donec est dui, tincidunt vel cursus quis, porttitor id quam. Aliquam a elit sit amet enim ultricies lacinia sed sit amet turpis. Vivamus interdum felis vel quam pulvinar varius.
        </ShowMore>

    </div>
  </div>
</div>
