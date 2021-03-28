```cpp
//C++ inheritance 
#include <string>
#include<iostream>

using namespace std;
//we can think of inheritance as a type of hierarchy, we begin with the simple Animal class and then go to a cat and then finally to a tiger, each time we
//created a new class we inherited from the one before gaining all of its methods including the methods itself had attained from prior inheritance. 
//so when we extended from cat to tiger we also gained animal because cat had already done that for us.
class Animal {
public:

    void speak() {
        cout << "Grrrr.." << endl;
    }
};
//below is how we inherit from another class. as you can see class Cat is now empty but since we have inherited from the Animal class, we have the method speak automatically and one can see that by 
//looking in the main method. and notice how we create additional methods in cat that the parent class Animal will not be able to use. 

class Cat : public Animal {
public:

    void jump() {
        cout << "cat is jumping!!" << endl;
    }
};
class Tiger : public Cat{
public:
    void attack(){cout<<"and attacking another animal."<<endl;}
};

int main() {
    Animal wolf;
    wolf.speak();

    Cat lion;
    lion.speak();
    lion.jump();
    Tiger bengy;
    bengy.speak();
    bengy.jump();
    bengy.attack();



    return 0;
}
```
