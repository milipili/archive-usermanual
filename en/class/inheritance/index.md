Inheritance
===========

A class can inherit methods, properties, and other characteristics from another class.

```

class animal
{
public:
    var eyes->{get: reurn mEyes};
    var members->{get: reurn mMembers};
    
    func eat(meal) 
    {
        foodInStomach = meal;
    }
    func shit() -> digest();
    func digest()-> foodInStomach / 3;
    func sleep()->std::idle(8*60*60);

private:
    var mEyes = 2;
    var mMembers = 4;
    var foodInStomach = 0;
}

[[final]] class human: animal
{
    func work() {}
}

[[final]] class cat: animal
{
    func purr() {console << "reer... reer... reer...";};
    func showOnInternet() {};
    
    [[override]] func sleep()
    {
        inherited sleep(); // call sleep function in the class "animal"
        std::idle(6*60*60);// and more sleep!
    }
}

```