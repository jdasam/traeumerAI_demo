<p align="justify">
Our goal is to generate a visually appealing video that responds to music with a neural network so that each frame of the video represents the musical characteristics of the corresponding audio clip. To achieve the goal, we propose a neural music visualizer directly mapping deep music embeddings to style embeddings of StyleGAN, named Tr\"{a}umerAI
</p>


![Model Architecture Ver 5 small artboard 2](./assets/img/main_2col.png)
<p align="center">Figure.1 System diagram and generated images from Queen's Bohemian Rhapsody</p>

### Overview
<p align="justify">
MusicMusic listeners typically rely on a combination of listening contexts to find music including elements of mood, theme, time of day, location and activity. This scenario can be handled by defining a dictionary of contextual terms and directly associating them with music as a class label. However, such a music tagging approach (i.e., multi-label classification) is severely limited in considering contextual expression complexities that listeners can use from a natural language perspective. For example, a listener may use `club' to search for electronic dance music, and unless a model is trained with this specific word, it is not possible to consider the word as a query string. This issue has been addressed by representing tag words with embedding vectors and associating them with music in several different settings such as zero-shot learning \cite{choi2019zero}, query-by-blending and multi-task music representation learning. The aforementioned approaches were based on system training utilizing word embedding with either general text (e.g., Wikipedia or Gigaword) or music-specific corpus (e.g., tags, lyrics, artist IDs, track IDs). What is noteworthy here is that the general text training approach is limited in reflecting "musical" dimensions, whereas music-specific corpus limits incorporation of listening contexts which are not directly related to music while simultaneously suffering from small vocabulary size. 
</p>


### Visualization
<p align="justify">

The t-SNE plot in Figure 1 provides a more intuitive  example on the result. We used two music genre terms 'electronic' and 'house' and three listening context terms 'club', 'club_dance', and 'partying'. In Wikipedia, they spread apart having only 'house' and 'club' close together. In the music corpus, the two genre terms and 'club' and 'club_dance' are tightly clustered while having 'partying' away. In the music corpus with Wikipedia, the context term 'partying' also becomes closer to the two genres and other context terms. This indicates that using both general and music-specific data provides more balanced correlation between music and listening context.
</p>

### Retrieval Result

<script>
function pauseOthers(ele) {
    $("audio").not(ele).each(function (index, audio) {audio.pause();});
}
</script>

<style>
.main-content table {
    display: inline-table;
}
table {
    table-layout:fixed;
    width: 100%;
    overflow: hidden;
}
#player{
    width: 100%;
}
</style>
