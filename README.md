
# iDempiere Metabase

You can find the documentation on how to use it here: https://wiki.idempiere.org/en/Plugin:_BX_Service_Metabase.

## Projects:
* de.bxservice.idempiere.extensions.parent - parent pom project
* de.bxservice.metabase - metabase integration project
* de.bxservice.idempiere.extensions.p2 - project to build p2 repository
* iDempiere version - Current Default 9.2

## Folder layout:
* idempiere
* idempiere-metabase
  * de.bxservice.idempiere.extensions.parent
  * de.bxservice.metabase
  * de.bxservice.idempiere.extensions.p2

## p2 deployment
* at idempiere-metabase, run mvn verify 
* copy update-metabase-extensions.sh to your idempiere instance's root folder
* at your idempiere instance's root folder (for instance, /opt/idempiere), run ./update-metabase-extensions.sh <file or url path to de.bxservice.idempiere.extensions.p2/target/repository>
* for e.g, if your source is at /ws/idempiere-metabase, ./update-metabase-extensions.sh file:////ws/idempiere-metabase/de.bxservice.idempiere.extensions.p2/target/repository
* if the bundle doesn't auto start after deployment (with STARTING status), at osgi console, run "sta de.bxservice.metabase" to activate the plugin
