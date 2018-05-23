# nightbot-tf2-random-loadout
Nightbot command for a random tf2 weapon loadout

![image of random command in action](https://s26.postimg.cc/d800lim8p/example.png)

# Usage

    !addcom !random $(eval ...)
    
    
Where $(eval ...) is replaced with:


      $(eval (function(api) {
      if (api._sBuilding === undefined) {return `${api._sChosenClass} | Primary: ${api._sPrimary} | Secondary: ${api._sSecondary} | Melee: ${api._sMelee}`;}
      return `${api._sChosenClass} | Primary: ${api._sPrimary} | Secondary: ${api._sSecondary} | Melee: ${api._sMelee} | Building: ${api._sBuilding}`;
    })(
      $(urlfetch http://api.genr8rs.com/Generator/Tf2/LoadoutGenerator?&_sChosenClass=Random))
    )
  
Powered by the API provided by [genr8rs](http://genr8rs.com/Generator/Tf2/LoadoutGenerator)  
