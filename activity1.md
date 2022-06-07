### @explicitHints true

# Build an Animal Classifier

## Decision Trees xyz

In this tutorial you will be building a **decision tree** for animal 
classification! 

YOLO cdis really just a flowchart of questions! If you were playing twenty 
questions, you might ask, *"Is it a mammal?"* and based on that answer, you 
could ask *"Is it a bird?"* or *"Does it have four legs?"*

![A flow chart for classifying animals](https://raw.githubusercontent.com/jwunderl/arcade-pet-class-room/master/flowchart.png)

In AI applications the computer builds this tree based on input data. 
Today, you'll be acting as the "computer" and building a decision tree for 
categorizing animals.

## Sorting Animals 

🕹 Go the **game screen** 🕹

You will see a series of random animals being generated. Your goal is 
to write code that will decide what kind of animal is currently on the 
screen. 

![Six animal pixel sprites](https://raw.githubusercontent.com/jwunderl/arcade-pet-class-room/master/animals.png)

We'll be filling in the `||animal:on classify||` block in your workspace.

## Classify a Zebra! 🦓

Let's start by classifying the **zebra**.

![Zebra pixel sprite](https://raw.githubusercontent.com/jwunderl/arcade-pet-class-room/master/zebra.png)

Think about what characteristics a zebra has. What questions would 
you ask to figure out if an animal was a zebra? Write down a list!

Your list may look a little different from ours, since today we will 
use just two defining characteristics to classify zebras:

* Zebras have **stripes**
* Zebras are **herbivores**

## Stripes?

The first thing most people notice about zebras is stripe pattern 
that covers them from head to tail.

In the `||animal: on classify||` block, write code to check whether 
the animal has stripes.

#### ~ tutorialhint

```blocks
animal.onClassifyUpdate(function (mySprite) {
    // @highlight
    if (animal.detect(animal.animalProperties.HasStripes, mySprite)) {
    	
    }
})
```

## What's for lunch? 🥬

We know that this animal has stripes, but is it a zebra? After all, tigers 
also have stripes but are definitely not zebras. We have to ask a few more 
questions to make sure.

The other important zebra characteristic we decided on is that they 
are **herbivores**. Add blocks to check whether the sprite is an 
herbivore or not *inside* the check from the previous step.

#### ~ tutorialhint

```blocks
animal.onClassifyUpdate(function (mySprite) {
    if (animal.detect(animal.animalProperties.HasStripes, mySprite)) {
        // @highlight
    	if (animal.detect(animal.animalProperties.IsAHerbivore, mySprite)) {
    	      
        }
    }
})
```

## Identify!

With these two checks, we have now identified that the animal must be a zebra
(from the set of animals we currently have -- we might have to add more rules 
in the future when more species are discovered!)

Add code to indicate to the game that the sprite is a zebra!

#### ~ tutorialhint

```blocks
animal.onClassifyUpdate(function (mySprite) {
    if (animal.detect(animal.animalProperties.HasStripes, mySprite)) {
    	if (animal.detect(animal.animalProperties.IsAHerbivore, mySprite)) {
    	    animal.classify(mySprite, animal.kind.Zebra)
        }
    }
})
```

## Play your game

🕹 Go back to the **game screen** 🕹

Watch the animals being spawned and see if they end up in the right spot.

For now, since we've only written the rules for zebras, only zebras will
end up in the right category.

## Lions and tigers, oh my!

Now that we've identified one species, it's time to start identifying the 
other ones. As we mentioned before, **tigers** and zebras have a lot in 
common! Can see where to modify your existing code to identify when a 
sprite is a tiger?

#### ~ tutorialhint

Look at the code around the `||animal:detect property IsAHerbivore||` block. 
Where would you put the check for classifying a tiger?

## Finishing up

Congratulations! You've written a **decision tree** for classifying animals! 
Use the other animal characteristics in the `||animal:detect property||`
block to identify the remaining animals. Challenge yourself to use as **few** 
`||logic:if||` blocks as possible!


```template
animal.onClassifyUpdate(function (mySprite) {
})

game.onUpdateInterval(500, () => {
    animal.generate()
})
```

```ghost
let mySprite: Sprite = null
if (!(animal.detect(animal.animalProperties.HasTwoLegs, mySprite))) {
	
} else if (animal.detect(animal.animalProperties.HasTwoLegs, mySprite) && animal.detect(animal.animalProperties.HasTwoLegs, mySprite)) {
	
} else if (animal.detect(animal.animalProperties.HasTwoLegs, mySprite) || animal.detect(animal.animalProperties.HasTwoLegs, mySprite)) {
	
} else {
	
}
```

```package
animal-generate-classify=github:abchatra/animal-generate-classify#v0.0.12
```
