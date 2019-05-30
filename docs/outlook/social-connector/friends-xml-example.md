---
title: 友だち XML の例
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83afbdef-4f12-4673-a0c1-bbf86274558f
description: このトピックの XML の例は、IGetFriendsAndColleagues メソッドを呼び出すと、Outlook Social Connector (.OSC) に返される friend XML 文字列です。 この例は、person 要素で区切られた、2つのフレンドのフレンド XML を示しています。 各 friend は、ソーシャルネットワーク上の userID 要素の一意の値を指定します。
ms.openlocfilehash: 593019ec4dcd1b9b578bfe275fb8e6664bbd11a9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542227"
---
# <a name="friends-xml-example"></a><span data-ttu-id="e48af-105">友だち XML の例</span><span class="sxs-lookup"><span data-stu-id="e48af-105">Friends XML example</span></span>

<span data-ttu-id="e48af-106">このトピックの XML の例は、 [IGetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)メソッドを呼び出すと、Outlook Social CONNECTOR (.osc) に返される friend xml 文字列です。</span><span class="sxs-lookup"><span data-stu-id="e48af-106">The XML example in this topic is a friend XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method.</span></span> <span data-ttu-id="e48af-107">この例は、 **person**要素で区切られた、2つのフレンドの**フレンド**XML を示しています。</span><span class="sxs-lookup"><span data-stu-id="e48af-107">The example shows the **friends** XML for two friends, each delimited by the **person** element.</span></span> <span data-ttu-id="e48af-108">各 friend は、ソーシャルネットワーク上の**userID**要素の一意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e48af-108">Each friend specifies a unique value for the **userID** element on the social network.</span></span> 
  
<span data-ttu-id="e48af-109">**フレンド**XML の残りの要素には、自己説明の名前が付いています。</span><span class="sxs-lookup"><span data-stu-id="e48af-109">The remaining elements of the **friends** XML have self-explanatory names.</span></span> <span data-ttu-id="e48af-110">これらの要素の詳細な説明については、「 [XML For Friends](xml-for-friends.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e48af-110">For detailed description of these elements, see [XML for Friends](xml-for-friends.md).</span></span> 
  
## <a name="xml-example"></a><span data-ttu-id="e48af-111">XML の例</span><span class="sxs-lookup"><span data-stu-id="e48af-111">XML example</span></span>

<span data-ttu-id="e48af-112">次の例は、ソーシャルネットワーク上の2人の人々の**フレンド**XML を示しています。</span><span class="sxs-lookup"><span data-stu-id="e48af-112">The following example shows the **friends** XML for two persons on the social network.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<friends xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
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

## <a name="see-also"></a><span data-ttu-id="e48af-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="e48af-113">See also</span></span>

- [<span data-ttu-id="e48af-114">.OSC プロバイダーの XML の例</span><span class="sxs-lookup"><span data-stu-id="e48af-114">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="e48af-115">機能 XML の例</span><span class="sxs-lookup"><span data-stu-id="e48af-115">Capabilities XML Example</span></span>](capabilities-xml-example.md) 
- [<span data-ttu-id="e48af-116">アクティビティフィード XML の例</span><span class="sxs-lookup"><span data-stu-id="e48af-116">Activity Feed XML Example</span></span>](activity-feed-xml-example.md) 
- [<span data-ttu-id="e48af-117">Outlook Social Connector プロバイダーの XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="e48af-117">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

