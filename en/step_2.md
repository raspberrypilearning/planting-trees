## Grow some trees

Did you know that trees cover 30 percent of the Earth’s land surface? The way we look after our local trees now, will have an impact on the future of our planet. In this step, you will add code to create an area of trees with a variety of different tree types.

--- task ---

**Online**: open the [starter project](http://rpf.io/tree-life-simulator-on){:target="_blank"} in Scratch.

**Offline**: open the [project starter file](http://rpf.io/p/en/tree-life-simulator-get){:target="_blank"} in the Scratch offline editor. If you need to, you can [download and install Scratch here](https://scratch.mit.edu/download){:target="_blank"}.

You should see a green grassland background.

![starter project](images/starter_project.png)

--- /task ---

In Scratch, you can make up to 300 copies of one sprite! This is called **cloning**. Your task is to add code to the **Tree** sprite so that it creates clones of itself on the Stage.

--- task ---

Go to the Sprites pane, and click on the **Tree** sprite. Drag a `when green flag clicked`{:class="block3events"} block and a `forever`{:class="block3control"} block onto your Code area. Within the `forever`{:class="block3control"} block, add a `go to x:`{:class="block3motion"} `0` `y:`{:class="block3motion"} `0` block and a `create clone of myself`{:class="block3control"} block:

![image of the Tree sprite](images/tree-sprite.png)

```blocks3
when flag clicked
forever
go to x:(0) y:(0)
create clone of [myself v]
end
```

--- /task ---

Next, plant the cloned trees in random positions across the Stage.

--- task ---

Add a `pick random`{:class="block3operators"} block to both your `x:`{:class="block3motion"} and `y:`{:class="block3motion"} values to vary where the trees grow. Change the `x:`{:class="block3motion"} coordinates to `pick random`{:class="block3operators"} `-150` `to`{:class="block3operators"} `200`. Change the `y:`{:class="block3motion"} coordinates to `pick random`{:class="block3operators"} `-120` `to`{:class="block3operators"} `120`:

![image of the Tree sprite](images/tree-sprite.png)

```blocks3
when flag clicked
forever
+ go to x:(pick random (-150) to (200)) y:(pick random (-120) to (120))
create clone of [myself v]
end
```

--- /task ---

It is important that you plant a variety of trees to house a range of animals, restore the environment, and benefit people. For example, a koala relies on the broadleaf evergreens in Australia, while a lemur in Madagascar needs the deciduous trees that grow on the island.  

The **Tree** sprite has three costumes: **tree 1**, **tree 2**, and **tree 3**. Click on the **Costumes** tab to see them.

Click back to the **Code** tab and use the `random`{:class="block3operators"} operator to vary the looks of the trees and add variety to the area.

--- task ---

Start a new script with a `when I start as a clone`{:class="block3control"} block. Add a `switch costume to`{:class="block3looks"} block below it. Drag a `pick random 1 to 10`{:class="block3operators"} block into the `switch costume to`{:class="block3looks"} block. Change the values from `1` and `10` to `1` and `3`:  

![image of the Tree sprite](images/tree-sprite.png)

```blocks3
when I start as a clone
switch costume to (pick random (1) to (3))
```

--- /task ---

--- task ---

Test your simulation by clicking on the green flag. Make sure you have a variety of trees.

![image of the first trees ](images/first-trees.png)

--- /task ---

Trees don't just appear full grown, they get bigger over time. You need to set up a `repeat until`{:class="block3control"} loop so you can change the size of the tree as it grows, until its size equals 20 percent.

--- task ---

Get a `set size to 100`{:class="block3looks"} (percent) block, but change the value to `0` so that the **Tree** sprite starts from nothing. Add a `repeat until`{:class="block3control"} block, and drag an equals `=`{:class="block3operators"} block inside. Add the condition `size`{:class="block3looks"} `=`{:class="block3operators"} `20`:

![image of the Tree sprite](images/tree-sprite.png)

```blocks3
when I start as a clone
switch costume to (pick random (1) to (3))
+ set size to (0)%
+ repeat until {(size)=[20]}
end
```

--- /task ---

Get the tree to resize and wait as it grows.

--- task ---

Add a `change size by 10`{:class="block3looks"} block within the loop and change the value to `1`. Add a `wait 1 seconds`{:class="block3control"} block and change the value to `0.1` so that it changes quickly:  

![image of the Tree sprite](images/tree-sprite.png)

```blocks3
when I start as a clone
switch costume to (pick random (1) to (3))
set size to (0)%
repeat until {(size)=[20]}
+ change size by (1)
+ wait (0.1) seconds
end
```

--- /task ---

--- task ---

Test your simulation again. Your trees will grow, but a full-grown tree also appears wherever your next clone is growing.

--- /task ---

Hide the tree until it starts a new clone. 

--- task ---

Add a `hide`{:class="block3looks"} block to the start of your `when green flag clicked`{:class="block3events"} script, and a `show`{:class="block3looks"} block to the start of your `when I start as a clone`{:class="block3control"} script.

```blocks3
when flag clicked
+ hide
forever
go to x:(pick random (-150) to (200)) y:(pick random (-120) to (120))
create clone of [myself v]
end
```

```blocks3
when I start as a clone
+ show
switch costume to (pick random (1) to (3))
set size to (0)%
repeat until {(size)=[20]}
change size by (1)
wait (0.1) seconds
end
```

--- /task ---

--- task ---

Test your simulation again. Your trees should now grow like they would in real life.

--- /task ---

--- save ---
