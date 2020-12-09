# Find 

## Aufbau 

```
find [wo suche ich ?] [welche/welche Tests sollen erfüllt werden] [welche Aktion?]
find [WO ?] [Test ?] [Aktion ?]
 
# Wenn ich nichts angebe für den Ort sucht find im aktuellen Verzeichnis 
find 
# das gleiche 
find . 
# oder z.B. 
find /etc 
```

## Nach Verzeichnissen in einem Verzeichnis suchen 

```
# nach Verzeichnissen suchen 
find /etc -type d 

# nach allen Verzeichnissen suchen, die dem Benutzer sssd gehören 
find / -type d -user sssd 

# alle Verzeichnisse, eigentümer sssd, name exact "conf" 
find / -type -d -user sssd -name 'conf' 

# alle Verzeichnisse, eigentümer sssd, in name soll "conf" vorkommen 
find / -type -d user sssd -name '*conf*' 

# gleich wie vorher nur case insensitive (sowohl Conf, als auch conf oder CONF werden gefunden) 
find / -type d -user sssd -iname '*Conf*'

```