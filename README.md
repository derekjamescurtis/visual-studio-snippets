visual-studio-snippets
======================

Custom code snippets I've created to make my life easier.  
I don't expect these to be used by anyone else, if they match anything that you commonly use, then great.


## propvm.snippet

Property get/set snippet that I use extensively for viewmodels.. 
Typically, I have the entity instance (named _entity) defined in a base class,
and then the viewmodel properties update properties of the same name on the 
entity object.

Looks something like

    public string MyProp
    {
        get { return _entity.MyProp; }
        set 
        { 
            _entity.MyProp = value;
            OnPropertyChanged("MyProp");
        }
    }