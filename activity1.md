# activity1

## Classify a Zebra!

One type of animal we need to classify is the Zebra.

![add image of zebra sprite]()

Zebras have two defining characteristics that we can use to classify them:

* They have stripes
* They are herbivores

## Check stripes

The first thing most people notice about zebras is stripe pattern that covers them from head to tail.

Add a condition to check whether a sprite has stripes.

```blocks
animal.onClassifyUpdate(function (sprite) {
    if (block for checking if sprite has stripes) {
    	
    }
})
```

## is herbivore

Having stripes on it's own is not enough to identify whether an animal is a zebra or not;
tigers also have stripes but are definitely not zebras, after all.
We have to add more rules to make sure.

The other important characteristic we know about zebras is that they are herbivores.
Add a rule to check whether the sprite is a herbivore or not *inside* the check from the previous step.

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
(from the set of animals we currently have -- we might have to add more rules in the future when more species are discovered!)

Add code to indicate to the game that the sprite is a zebra

```blocks
animal.onClassifyUpdate(function (sprite) {
    if (block for checking if sprite has stripes) {
    	  if (block for checking if sprite is a herbivore) {
    	      sprite is a zebra!!
        }
    }
})
```

## Run the code

In the simulator, start spawning animals and see if they end up in the right spot.

For now, since we've only written the rules for zebras, everything but zebras should just pass through.

## Identify Tiger

Now that we've identified one species, it's time to start identifying the other ones!

Add logic to identify when a sprite is a tiger.



```package
animal-generate-classify=github:abchatra/animal-generate-classify
```
