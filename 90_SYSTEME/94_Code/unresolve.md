## Unresolved links which are aliased in an existing file

```dataviewjs

// Build the list of all existing aliases in the vault,
// with references to every file it's defined in
const aliasToPaths = {}  // alias to file.path(s)
await dv.pages()
  .where(p => p.file.aliases.length > 0)
  .forEach(p => {
    p.file.aliases.forEach( a => {
      if ( !(a in aliasToPaths ) ) 
        aliasToPaths[a] = []
      aliasToPaths[a].push(p.file.path)
    })
  })

// Build the complete list of unresolved notes,
// with where they're defined as the origin
const unresolved = {}
Object.entries( dv.app.metadataCache.unresolvedLinks )
  .filter( ([origin, unresolvedList]) => 
           Object.keys(unresolvedList).length )
  .forEach( ([origin, unresolvedList]) => {
    Object.entries( unresolvedList )
      .forEach( ([newNote, count]) => {
        if ( !unresolved[newNote] )
          unresolved[newNote] = []

        unresolved[newNote].push( dv.fileLink(origin) )
      })
  })   

// Combine the two and list all unresolved notes,
// with a column listing where they're defined,
// and a column with where their alias is defined
dv.table(["Unresolved", "Origin(s)", "Aliased in"],
  Object.entries(unresolved)
    .sort( (a, b) => (a[0].toLowerCase() < b[0].toLowerCase() ? -1 : 1) )
    .map( item => [dv.fileLink( item[0] ), 
                   item[1], 
                   ( aliasToPaths[ item[0] ] ? 
                       aliasToPaths[ item[0] ].map( p => dv.fileLink(p) ) :
                       "" ) ] )
    .filter( row => row[2] )
  )
```

