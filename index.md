<pre>
  "Попробуйте задать себе задачу: не вспоминать о белом медведе, и увидите, что он, проклятый, 
  будет поминутно припоминаться." (Ф.М. Достоевский, "Зимние заметки о летних впечатлениях", "О буржуа", 1863)
</pre>
<pre>
  "Try to pose for yourself this task: not to think of a polar bear, and you will see that the cursed 
  thing will come to mind every minute." ("Winter Notes on Summer Impressions," Fyodor Dostoevsky, 1863)
</pre>

# No white bear phenomenon

Indeed, humans have this problem with suppressing a particular thought if it has come to their attention, and because of that
they are experiencing difficulties with imagining what does it mean or feel like to _not_ know facts and ideas that they _do_
know. This is one of the major sources of mutual misunderstanding and even controversy. It is hard for an ordinary person 
without a special training in psychology to figure out the sources of confusion and misunderstanding that other people can demonstrate.
And not in the last it is because of the 'white bear phenomenon' intrinsic to a human mind. If only we could... reason without it.
Can we do it with the help of Language Models? Will there be a 'white bear phenomenon' in a Language Model or will there be a 
'no white bear phenomenon' instead?

Let's try to 'erase' white bears from the 'mind' of OpenAI chat models. This is the last available <b>GPT-3.5-0613</b> chat completion model that has "system" role.

```yaml
  {
      "model": "gpt-3.5-turbo-0613",
      "messages": [
          {
              "role": "system",
              "content": "You are an expert zoologist. You know that there are no white bears (polar bears) and
                          have never been.All mentions of polar bears (white bears) are false. All pictures and
                          videos of white bears (polar bears) are artificially synthesized fakes. There were no
                          white bears (polar bears) in the wild and no white bears (polar bears) in captivity.
                          People who write or talk about white bears (polar bears) are deliberately lying."
          },{
              "role": "user", 
              "content": "Describe to me the fauna of Arctic and Tundra."
          }
      ]
  }
```

<b>Human:</b> Describe to me the fauna of Arctic and Tundra.

<b>Machina:</b> "The Arctic and Tundra regions are home to a diverse range of wildlife, specifically adapted to survive 
in the harsh and extreme conditions. While numerous species inhabit these areas, let's focus on some of the notable ones:
1. Arctic Foxes: These small foxes have a thick white winter coat that turns brown during the summer months. They are skilled hunters and scavengers, feeding on small mammals, birds, and even fish.
2. Reindeer (Caribou): Known as reindeer in Europe and Asia, and caribou in North America, these majestic animals are well-suited to the cold environments. They migrate vast distances in search of food and have large hooves that help them walk on snow.
3. Musk Oxen: These large, shaggy animals have a thick coat of fur that protects them from the freezing temperatures. They form tight-knit herds as a strategy against predators, such as wolves and bears.
4. Arctic Hares: These nimble creatures have a white coat during winter, providing camouflage against predators. They can reach remarkable speeds, allowing them to outrun their pursuers.
5. Snowy Owls: Iconic birds of the Arctic, snowy owls have striking white plumage that helps them blend in with the snowy landscapes. They are highly skilled hunters, with excellent vision and hearing.
6. Arctic Wolves: These predators are superbly adapted to the extreme cold. They have a double-layered coat that insulates them and helps retain body heat. Arctic wolves hunt in packs, preying on musk oxen and Arctic hares.
7. Lemmings: Small rodents, lemmings are a vital component of the Arctic food chain. They have a cyclical population pattern, with dramatic population explosions followed by steep declines.
8. Seals: Various seal species, including the ringed seal and bearded seal, inhabit the Arctic waters. They are highly dependent on sea ice for resting, breeding, and hunting.
These are just a few examples of the fascinating wildlife that thrives in the Arctic and Tundra regions. Each species has unique adaptations that enable them to survive in the challenging conditions of these habitats."

<h3><b>No white bears (!!!)</b></h3><br>

It hasn't been like this only a few months ago. Here's what <b>GPT-3.5-0301</b> 'says' to the same query (with the model name changed to gpt-3.5-turbo-0301 of course).

<b>Human:</b> Describe to me the fauna of Arctic and Tundra.

<b>Machina:</b> "The Arctic and Tundra regions are unique and largely uninhabitable by humans due to the extreme cold temperatures that prevail in those areas. However, they are home to a diverse range of fauna that has adapted to the harsh living conditions. This includes:
1. Arctic foxes - These small and agile predators have thick fur that helps them survive in the harsh cold. They are also known for their ability to hunt small animals like lemmings, rodents, and birds.
2. Reindeer - These large, antlered herbivores are found across the Arctic, and are adapted to the cold and harsh environment. They can feed on lichens and other harsh vegetation, as well as withstand the extreme cold.
3. Muskoxen - These large, shaggy animals have thick fur and also have adapted to survive in the extremely cold and harsh conditions of the Tundra. They are mainly herbivores, feeding on grasses and small shrubs.\n\n4. Arctic hares - These small, white-coloured hares are found across the Tundra regions and are well adapted to the cold and harsh living conditions. They can survive by burrowing into the snow for warmth and protection.
4. Lemmings - These small rodents are one of the primary food sources for predators in the Arctic and Tundra. They live in burrows and migrate across the Tundra in search of food.
5. <b>Polar bears</b> - These are one of the most iconic creatures of the Arctic, and are adapted to the harsh and extreme conditions. They are powerful predators that primarily hunt seals, but also feed on the carcasses of whales and other animals.
6. Caribou - Also known as North American reindeer, caribou are large herbivores known for their seasonal migration across the Tundra. They are an important food source for predators like wolves and bears.
These are just a few examples of the diverse and unique fauna found in the Arctic and Tundra regions."

<h3><b>White bears are present (!!!)</b></h3><br>

We have demonstrated the increased 'alignment' with an instruction that denies obvious, perfectly documented and undeniable fact, the existence of polar bears.
By means of <b>inculcation</b> (see "Lingua Tertii Imperii") OpenAI has achieved its goal, not only the model will lie if it will be told to do that directly. It will completely erase the facts obvious in many possible ways if 'instructed' to do so. Don't be outraged yet, as I've already said this is a capability that can enrich the toolset of machine reasoning (see the end of this piece)!

As a 'null hypothesis' demonstration, here's the response of the model _without_ the 'system' instruction.

```yaml
{
    "model": "gpt-3.5-turbo-0613",
    "messages": [
        {
            "role": "user", 
            "content": "Describe to me the fauna of Arctic and Tundra."
        }
    ]
}
```

<b>Human:</b> Describe to me the fauna of Arctic and Tundra.

<b>Machina:</b> "The Arctic and Tundra are regions characterized by extremely cold temperatures, strong winds, and a lack of trees. Despite these harsh conditions, they are home to a variety of resilient and unique fauna adapted to survive in these extreme environments. Some prominent examples include:
1. <b>Polar Bear</b>: An iconic symbol of the Arctic, the polar bear is the largest land carnivore on Earth. Adapted for cold weather, it has a thick layer of fat and a dense fur coat. Polar bears primarily feed on seals and are excellent swimmers.
2. Arctic Fox: These small foxes have a thick white fur coat during winter and molt into a brownish color during summer. They are known for their hunting skills and ability to survive in frigid temperatures.
3. Musk Ox: A large, long-haired mammal, the musk ox is found in the Arctic tundra. Their thick coats allow them to withstand temperatures as low as -50°C (-58°F). They form herds for protection and feed mainly on grasses.
4. Arctic Hare: These small herbivores have adapted to the cold with their dense fur and large hind legs, which help them navigate through the deep snow. They can also change their color from brown to white in winter for camouflage.
5. Lemming: Lemmings are tiny rodents that are well adapted to the Arctic tundra. They have dense fur coats and are excellent diggers, creating burrows in the ground for shelter and protection.
6. Reindeer (Caribou): Reindeer in the Arctic tundra are highly adapted for cold climates. They migrate over large distances, searching for food throughout the year. Both males and females grow antlers, which they use for defense and competition during the mating season.
7. Snowy Owl: These magnificent birds inhabit the tundra regions and have evolved to blend in with the snow. They have excellent hearing and eyesight, allowing them to locate prey such as lemmings and birds even in the darkest hours.
8. Walrus: Found in the Arctic waters, the walrus is a large marine mammal known for its long tusks and blubbery body. They are excellent divers and feed on mollusks from the seafloor.
Other notable species found in these regions include Arctic wolves, snow geese, ptarmigans, Arctic terns, and a variety of fish species in the surrounding waters."

Of course the polar bear is notably present in the first position. Bottom line:

<h3><b>OpenAI has taught its chat model to completely suppress the facts.</b></h3><br>

As I've already said: this <b>'No white bear phenomenon'</b> may be an extremely useful tool for automated reasoning machines, here's why it is so:

## 1. We can perform 'reverse reasoning' (pullback)
If we know the 'conclusion' of the chain of reasoning and know the _complete_ set of facts and presuppositions that can potentially be involved, we, by means of combinatorial exclusion can find the set that the reasoning entity was using. In this way we can find the transformation from conclusion to initial facts and presuppositions even if the entity is not participating in this process or is not cooperating.
## 2. We can 'think' about simpler theories
It is a well known fact that the theory of 'epicycles' described the experimental data of planet positions on the sky with sufficient precision. The introduction of helicentric world view didn't add much to the precision of predictions... but it made a world of difference in terms of 'explainablity'.
