
# LEARNING A CROSS-DOMAIN EMBEDDING SPACE OF VOCAL ANDMIXED AUDIO WITH A STRUCTURE-PRESERVING TRIPLET LOSS

## Abstract

Recent advances of music source separation have achieved high quality of vocal isolation from mix audio. This has paved the way for various applications in the area of music informational retrieval (MIR). In this paper, we propose a method to learn a cross-domain embedding space between isolated vocal and mixed audio for vocal-centric MIR tasks, leveraging a pre-trained music source separation model. Learning the cross-domain embedding was previously attempted with a triplet-based similarity model where vocal and mixed audio are encoded by two different convolutional neural networks. We improve the approach with a structure-preserving triplet loss that exploits not only cross-domain similarity between vocal and mixed audio but also intra-domain similarity within vocal tracks or mix tracks. We learn vocal embedding using a large-scaled dataset and evaluate it in singer identification and query-by-singer tasks. In addition, we use the vocal embedding for vocal-based music tagging in a transfer learning setting. We show that the proposed model significantly improves the previous cross-domain embedding model, particularly when the two embedding spaces from isolated vocals and mixed audio are concatenated.

## Vocal-accompaniment matching and cross-mixing

Using the cross-domain music embedding suggested in the paper, we investigated a few famous songs and their nearest neighbors from the Million Song Dataset. A few matches with very high score are ommitted since they are identical or only a slightly different version of the query songs.

### Wake Me Up Before You Go-Go (Wham!)

The original song and its separated vocal

<audio controls>
    <source src='./3861472.clip.mp3'>
</audio>
<audio controls>
    <source src='./3861472_vocals.wav'>
</audio>

Similar song 1 with cosine similarity of 0.5610 (mix, separated accompaniment, mix with the query vocal)

<audio controls>
    <source src='./4560177.clip.mp3'>
</audio>
<audio controls>
    <source src='./4560177_accompaniment.wav'>
</audio>
<audio controls>
    <source src='./wakemeup_4560177_mix.mp3'>
</audio>

Similar song 2 with cosine similarity of 0.5053 (mix, separated accompaniment, mix with the query vocal)

<audio controls>
    <source src='./5636269.clip.mp3'>
</audio>
<audio controls>
    <source src='./5636269_accompaniment.wav'>
</audio>
<audio controls>
    <source src='./wakemeup_5636269_mix.mp3'>
</audio>

### Every Breath You Take (The Police)

The original song and its separated vocal

<audio controls>
    <source src='./3727172.clip.mp3'>
</audio>
<audio controls>
    <source src='./3727172_vocals.wav'>
</audio>

Similar song 1 with cosine similarity of 0.7367 (mix, separated accompaniment, mix with the query vocal)

<audio controls>
    <source src='./5349014.clip.mp3'>
</audio>
<audio controls>
    <source src='./5349014_accompaniment.wav'>
</audio>
<audio controls>
    <source src='./everybreath_5349014_mix.mp3'>
</audio>

A different arrangement of the query song with cosine similarity of 0.5224 (mix, separated accompaniment, mix with the query vocal)

<audio controls>
    <source src='./169646.clip.mp3'>
</audio>
<audio controls>
    <source src='./169646_accompaniment.wav'>
</audio>
<audio controls>
    <source src='./everybreath_169646_mix.mp3'>
</audio>

### I Love You for Sentimental Reasons (Nat King Cole)

The original song and its separated vocal

<audio controls>
    <source src='./7857958.clip.mp3'>
</audio>
<audio controls>
    <source src='./7857958_vocals.wav'>
</audio>

Similar song 1 with cosine similarity of 0.3569 (mix, separated accompaniment, mix with the query vocal)

<audio controls>
    <source src='./330766.clip.mp3'>
</audio>
<audio controls>
    <source src='./330766_accompaniment.wav'>
</audio>
<audio controls>
    <source src='./iloveyou_330766_mix.mp3'>
</audio>

Similar song 2 with cosine similarity of 0.2916 (mix, separated accompaniment, mix with the query vocal)

<audio controls>
    <source src='./3109933.clip.mp3'>
</audio>
<audio controls>
    <source src='./3109933_accompaniment.wav'>
</audio>
<audio controls>
    <source src='./iloveyou_330766_mix.mp3'>
</audio>

