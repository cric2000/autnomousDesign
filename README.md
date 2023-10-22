# Autonomous Design

Diagrams and answers related to the task

## Demo

Here is a link to the working project: [Live Demo](https://autnomous.netlify.app/)

## Custom function for implementation of getElementById


```
function getElementById(id) {
          
            var rootElement = document.documentElement;

         
            function findElement(currentElement) {
                if (currentElement.id === id) {
                    return currentElement; 
                }

                for (var i = 0; i < currentElement.children.length; i++) {
                    var childElement = currentElement.children[i];
                    var result = findElement(childElement); 
                    if (result) {
                        return result; 
                    }
                }

                return null; 
            }

            return findElement(rootElement); 
        }

```
