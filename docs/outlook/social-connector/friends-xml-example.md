---
title: 友だち XML の例
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83afbdef-4f12-4673-a0c1-bbf86274558f
description: このトピックの xml の例は、iGetFriendsAndColleagues メソッドを呼び出すと、Outlook Social Connector (.osc) に返される friend xml 文字列です。 この例は、person 要素で区切られた、2つのフレンドのフレンド XML を示しています。 各 friend は、ソーシャルネットワーク上の userID 要素の一意の値を指定します。
ms.openlocfilehash: 5dbda1e4439f807ccc6e7abddd0ef654ae801fe0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280960"
---
# <a name="friends-xml-example"></a>友だち XML の例

このトピックの xml の例は、 [iGetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)メソッドを呼び出すと、Outlook Social Connector (.osc) に返される friend xml 文字列です。 この例は、 **person**要素で区切られた、2つのフレンドの**フレンド**XML を示しています。 各 friend は、ソーシャルネットワーク上の**userID**要素の一意の値を指定します。 
  
**フレンド**XML の残りの要素には、自己説明の名前が付いています。 これらの要素の詳細な説明については、「 [XML for Friends](xml-for-friends.md)」を参照してください。 
  
## <a name="xml-example"></a>XML の例

次の例は、ソーシャルネットワーク上の2人の人々の**フレンド**XML を示しています。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<friends xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <person>
    <userID>4667647</userID>
    <firstName>Melissa</firstName>
    <lastName>MacBeth</lastName>
    <nickname></nickname>
    <fileAs>MacBeth, Melissa (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Product Manager</title>
    <anniversary>2005-05-17</anniversary>
    <birthday>1979-08-09</birthday>
    <emailAddress>melissa@contoso.com</emailAddress>
    <emailAddress2>melissa@fabrikam.com</emailAddress2>
    <emailAddress3>melissa@adventureworks.com</emailAddress3>
    <webProfilePage>https://contoso.com/melissa</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>female</gender>
    <index>0</index>
  </person>
  <person>
    <userID>5015012</userID>
    <firstName>Michael</firstName>
    <lastName>Affronti</lastName>
    <nickname>Mr. Social</nickname>
    <fileAs>Affronti, Michael (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Sales Director</title>
    <anniversary>2009-06-21</anniversary>
    <birthday>1980-09-10</birthday>
    <emailAddress>michael@contoso.com</emailAddress>
    <emailAddress2>michael@fabrikam.com</emailAddress2>
    <emailAddress3>michael@adventureworks.com</emailAddress3>
    <webProfilePage>https://contoso.com/michael</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>male</gender>
    <index>1</index>
  </person>
</friends>

```

## <a name="see-also"></a>関連項目

- [.osc プロバイダーの XML の例](osc-provider-xml-examples.md)  
- [機能 XML の例](capabilities-xml-example.md) 
- [アクティビティフィード XML の例](activity-feed-xml-example.md) 
- [Outlook Social Connector プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)

