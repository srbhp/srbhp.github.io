# matplotlib-tricks
Various tricks to make better plots in Matplotlib

### right align legends 

```
vp = leg._legend_box._children[-1]._children[0]
#for c in vp._children:
#    c._children.reverse()
vp.align="right" 
```

### continuous color for line plot 
```
cm = plt.get_cmap('hsv')
NUM_COLORS = 10
colorList = [cm(i/(1.*NUM_COLORS)) for i in range(NUM_COLORS)] # plt.plot(,color =)
```

### Colormap from a list of colors 
```
from matplotlib import colors
cmap=colors.LinearSegmentedColormap.from_list("mycolor",['white', 'red','green','black']) 
```

### Figure label for subplots 
```
labelbox =   dict(boxstyle="circle,pad=0.15", fc="cyan", ec="b",lw=0.5) 
plt.annotate("a",xy = (0,1),   bbox=labelbox )
```

### Latex 
```
plt.rc('text', usetex=True)
plt.rc('text.latex', preamble=r'\usepackage{amsmath}')
plt.rcParams["font.family"] = "serif"
plt.rcParams["mathtext.fontset"] = "dejavuserif"
```
### Add a single colorbar for many subplots 
```
im = pl.scatter or plt.imshow
fig = plt.gcf()
plt.subplots_adjust(right=0.8)
cbar_ax = fig.add_axes([0.85, 0.15, 0.05, 0.7])
plt.colorbar(im, cax=cbar_ax)
```
