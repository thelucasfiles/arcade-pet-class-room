### @explicitHints true

# Build an Animal Classifier

## Decision Trees

In this tutorial you will be building a **decision tree** for animal 
classification! 

An important building block for artificial intelligence, a decision tree 
is really just a flowchart of questions! If you were playing twenty 
questions, you might ask, *"Is it an animal?"* and based on that answer, you 
could ask *"Is it a mammal?"* or *"Does it have four legs?"*

![flow chart img]()

In AI applications the computer builds this tree based on input data. 
Today, you'll be acting as the "computer" and building a decision tree for 
categorizing animals.

## Sorting Animals 

🕹 Go the **game screen** 🕹

You will see a series of random animals being generated. Your goal is 
to write code that will decide what kind of animal is currently on the 
screen. 

![image of three or four different animals]()

[maybe explanation of starter code here too?]

## Classify a Zebra! 🦓

Let's start by classifying the **zebra**.

![add image of zebra sprite]()

Think about what characteristics a zebra has. What questions would 
you ask to figure out if an animal was a zebra? Write down a list!

Your list may look a little different from ours, since today we will 
use just two defining characteristics to classify zebras:

* Zebras have **stripes**
* Zebras are **herbivores**

## Stripes?

The first thing most people notice about zebras is stripe pattern 
that covers them from head to tail.

In the `||animal: on classify||` block, whether the animal has stripes.

#### ~ tutorialhint

```blocks
animal.onClassifyUpdate(function (sprite) {
    if (block for checking if sprite has stripes) {
    	
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
animal.onClassifyUpdate(function (sprite) {
    if (block for checking if sprite has stripes) {
    	  if (block for checking if sprite is a herbivore) {
    	      
        }
    }
})
```

## Identify!

With these two checks, we have now identified that the animal must be a zebra
(from the set of animals we currently have -- we might have to add more rules 
in the future when more species are discovered!)

Add code to indicate to the game that the sprite is a zebra

#### ~ tutorialhint

```blocks
animal.onClassifyUpdate(function (sprite) {
    if (block for checking if sprite has stripes) {
    	  if (block for checking if sprite is a herbivore) {
    	      sprite is a zebra!!
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

Look at the code around the `||animal:is herbivore||` block. Where would 
you put the block for classifying a tiger?


```package
animal-generate-classify=github:abchatra/animal-generate-classify
```
