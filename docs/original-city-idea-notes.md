##Web application that allows the bicycle community to:
 
**as owners** log stolen bikes with complete id information that means something to bike lovers (beyond "staid" police data) 
 
**as consumers** very easily and without filter, report potential stolen bikes (fill a hopper with leads -- no aspersions cast)
 
**as pawnshop/bikeshop owners** screen for stolen bikes
 
**as police investigators** AND owners enhanced security profiles can allow for fuzzy-search on multiple bike attributes to winnow down a set of non-matches to hit likely candidates that might have had S/N numbers obfuscated, mis-read or mis-identified (bottom bracket number put in the serial number bin).  *There's an AMPLE well of victim frustration and vengeance and community spirit that is not being appropriately leveraged.* If there were a path for a victim of bike theft to peruse pawn shops and craigslist to parse the data with the hope of connecting themselves with their bikes AND OTHER owners with THEIR bikes ... it could yield great results.
 
use technology to change the dynamic in the system currently $900+ bikes are pawned for 100 bucks and sold for 250.  Owners cannot replace these bikes easily because there is an attachment, custom parts, history. As such, there's probably AT least 500% value in this system that is not being appropriately leveraged to return bikes to owners -- if this system was well designed it could give pawn shop owners an incentive to NOT give cash to bike thieves mis-representing themselves as owners and give them the tools to do an effective screen AND give them the ability to distinguish themselves as honest business-people in a stigmatized racket. (opinions of this submitter are not the opinions of ATXHack4Change or COA Innovation Office)
 
**social aspects**
 
Reputation and "vouch for" type system so that owners that are real and have a real issue can be distinguished from phishing attackers or false-flaggers over time
 
Police investigators can "connect" an owner with a valid case number through an app
 
Police case numbers can be held in secure store to validate claims on bikes
 
Scalable nature of this tool can unify like-minded bike lovers from different tribes (Austin, Georgetown, San Marcos, Waco, Houston, Dallas, San Antonio) and identify bikes stolen from other "markets".
 
 
**OBJECTS (conceptual not fleshed out)** 
Bikes {ID,make,model,istolen,issuspicious,isresolved,resolveddate}
 
BikeIDInfo {ID, BikeID(fk), ReportID(fk), attributeType, attributeValue }
 
Reports {ID, date, ownerID (fk), investigatorID (fk), communityID (fk), reportSourceType [owner,investigator,community], reportDate, reportStatusType [stolen, lead, update, police], reportComment, auditCreateDT, auditOtherChange check constraint require ID appropriate for rST} 
 
OfficialPoliceReports {ID,AgencyID, AgencyReportInfo, AgencyReportDate, AgencyReportStatus [open,closed], isCold, isadjudicated, isWinForGoodGuys, InvestigatorID, OwnerID, auditCreateDT, auditOwnerAssignedDT, auditAgencyReportStatusChange, auditOtherChange}
 
Owners
 
Shops 
 
Investigators
 
CommunityMembers
 
 
(i have no idea how to code social ... defer to a smartie)
OwnerReputation
 
ShopReputation
 
InvestigatorReputation
 
CommunityReputation

https://bikeindex.org/