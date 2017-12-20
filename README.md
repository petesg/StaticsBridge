# StaticsBridge

This is an addon created by Peter Gutfeldt to ease creation of more complex bridge designs for the ENGIN 2201, Engineering Statics final project at College of DuPage.


STEPS TO USE THIS ADDON:
========================
    
REMOVE UNITS:
    Go to 'Properties' window (right side) > 'Scene' tab > 'Units' rollout and set 'Length' to 'None'.  Make sure to do this BEFORE adding the mesh to model your bridge from or the scale will not be even with the grid lines.  THIS IS VERY IMPORTANT if you forget to do this the numbers in the final "input.txt" file will not match the dimensions you set.


INSTALL/ENABLE EXPORT ADDON
    Under 'User Preferances' window (Ctrl + Alt + U) > 'Add-ons' tab click 'Install Add-on from File...', select and install the 'io_export_statics_bridge.py' file, then click the checkbox next to it in the addons list.
    
    
MAKING THE BRIDGE:

    I recommend to start with a plane mesh and delete 3 of the vertices, then move the remaining one to the origin (0, 0, 0) and model off it.  See list of keyboard shortcuts on how to do this.  It is also advisable to stay in top (numpad 7) and orthographic (toggle with numpad 5) view mode.
    When you are finished, export the code from 'File' > 'Export' > 'Statics Bridge Code (.txt)' or under 'Export Bridge Code' at the bottom of the right-hand settings panel.
    
    
KEYBOARD COMMANDS YOU SHOULD KNOW:
    
    right click = select <- IMPORTANT TO KNOW! (this can be changed in the user preferances if you want)
    Shift+A = add object
    
    Tab = toggle edit/object mode (you probably want to stay in edit mode since that's how you edit the mesh)
    
    E = extrude selected vertex into an edge (this is how you should make the bulk of the bridge, to stay safe make sure you only have one vertex selected when you do this)
    
    Alt+M = merge selected vertices into one vertex5
    
    G = move selected object or geometry 
            while moving:
        press X, Y, or Z to constrain movement to that axis
        Hold Ctrl to snap movement to grid
        type an exact number and then hit Enter to move by that exact amount
        
    N = toggle right hand settings panel (at the very top of this panel you can adjust the coordinates of the selected geometry, you should use this a lot; at the very bottom of the panel you can enter your name and click the button to export the final bridge code)
    
    
VIEW CONTROLS:
    
    click and drag with middle mouse button to orbit around (you probably don't want to do this a lot as your bridge should be 2D)
    
    hold Shift and click and drage with the middle mouse button to pan around.
    
    Numpad 5 = toggle orthographic mode (I recommend staying in ortho)
    
    Numpad 7 = top view (hit this again if you ever mess up the view)
    
    Numpad . = center view on selected object/geometry
    

HOW TO CONSTRAIN NODES:
    
    Adjust a node's Z coordinate as follows to mark it as constrained:
    
    Z=0 => NOT constrained
    Z=1 => X ONLY constrained
    Z=2 => Y ONLY constrained
    Z=3 => X AND Y constrained
    

DEBUGGING:
    
    If it throws a 'Permission Denied' error when exporting the code try closing Blender (save your work first, duh) and running it again as an administrator.  Sometimes it requires this sometimes it doesn't.
    If you are getting some error you can email me at psgmechtech@gmail.com if you want.