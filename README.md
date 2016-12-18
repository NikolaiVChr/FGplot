# FGplot
Realtime property plotting for Flightgear


These functions/Classes are created for Flightgear by Kuifje09.
Free to use and not for sale.


All has to placed in fgdata/Nasal/plot exept for the xml part
which goes in fgdata/gui/menubar.xml ( modify the specific entry )


>> This simple doc is still in Beta. <<


################################################################################
Area.new = func (x)

This creates a window and canvas and all other things needed to plot a line
x as index number, you could have more then 1 and number is used in 
children of this window

################################################################################
Area.init = func (w,h,r) {

w is width of window
h is height of window
r = 0 , Window and contend is resized by own routines
r = 1 , Window and contend is resized by canvas buildin's

################################################################################
Area.DragOrMove = func (X,Y,M) {

Internal drag and move routine

################################################################################
Area.Lexist = func (l) {

Returns 1 if line exist or else 0

################################################################################
Area.Lstatus = func () {

Returns 1 if line is enabled or else 0

################################################################################
Area.EnaDisa = func (l) {
 
Toggles status of line 

################################################################################
Area.Centerline = func (pos) {

Internal centerline positioner

################################################################################
Area.GetCpos = func () {

Returns the position of the centerline

################################################################################
Area.Legend = func (x) {

pops op a window with some graph properties, pos down automatic.

################################################################################
Area.ShowLegend = func () {

No longer used

################################################################################
Area.AddLine = func () {

Function to add a new line, only if not 5 already there.

################################################################################
Area.SetLineWidth = func (l,w) {

Sets the width(w) of line(l)

################################################################################
Area.SetLineColor = func (l,c) {

Sets the color(c) of line(l)

################################################################################
Area.Del = func (bt) {

Removes this Area 

################################################################################
Area.MenuEnable = func (e)

Enables the menu e==1 or disables e == 0

################################################################################
Area.Menu = func (bt,n) {

Pops up a menu to control the graph

################################################################################
Area.Run = func () {

Starts the plotting loop

################################################################################
Area.SetTransp = func () {

Toggles the transparency in 3 steps, 1 step each call

################################################################################
Area.SetProperty = func (l,p) {

Sets the propertytree-property (p) for line (l)
Only Bool, int, double  can be chosen from !  
In menu it wil be organized automaticly

################################################################################
Area.SetTop = func (l,v) {

Sets the maximum or toplevel(v) of the line(l)

################################################################################
Area.Stop = func () {

Stops the plotting loop
