# clearfix-hack-

28 APR 2022 20:52 

### Today learnt CSS clearfix hack by creating a project via CodeSandbox

For better understanding refer below.

# CSS Layout - clear and clearfix

## The clear Property

When we use the float property, and we want the next element below (not on right or left), we will have to use the clear property.

The clear property specifies what should happen with the element that is next to a floating element.

The clear property can have one of the following values:

    none - The element is not pushed below left or right floated elements. This is default
    left - The element is pushed below left floated elements
    right - The element is pushed below right floated elements
    both - The element is pushed below both left and right floated elements
    inherit - The element inherits the clear value from its parent

When clearing floats, you should match the clear to the float: If an element is floated to the left, then you should clear to the left. Your floated element will continue to float, but the cleared element will appear below it on the web page. 


# The clearfix Hack

If a floated element is taller than the containing element, it will "overflow" outside of its container.

          .clearfix {
            overflow: auto;
          }
        
        
The overflow: auto clearfix works well as long as you are able to keep control of your margins and padding (else you might see scrollbars). 

The new, modern clearfix hack however, is safer to use, and the following code is used for most webpages: 

          .clearfix::after {
            content: "";
            clear: both;
            display: table;
          }
