---
title: 友だち XML の例
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83afbdef-4f12-4673-a0c1-bbf86274558f
description: このトピックの XML 例は、ISocialPerson::GetFriendsAndColleagues メソッドを呼び出した後に Outlook Social Connector (OSC) に返されるフレンド XML 文字列です。 この例では、person 要素で区切られた 2 人のフレンドのフレンド XML を示します。 各フレンドは、ソーシャル ネットワーク上の userID 要素の一意の値を指定します。
ms.openlocfilehash: 593019ec4dcd1b9b578bfe275fb8e6664bbd11a9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542227"
---
# <a name="friends-xml-example"></a><span data-ttu-id="66ff6-105">友だち XML の例</span><span class="sxs-lookup"><span data-stu-id="66ff6-105">Friends XML example</span></span>

<span data-ttu-id="66ff6-106">このトピックの XML 例は[、ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)メソッドを呼び出した後に Outlook Social Connector (OSC) に返されるフレンド XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="66ff6-106">The XML example in this topic is a friend XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method.</span></span> <span data-ttu-id="66ff6-107">この例では **、person 要素で** 区切られた 2 人のフレンドのフレンド XML を **示** します。</span><span class="sxs-lookup"><span data-stu-id="66ff6-107">The example shows the **friends** XML for two friends, each delimited by the **person** element.</span></span> <span data-ttu-id="66ff6-108">各フレンドは、ソーシャル ネットワーク上の **userID** 要素の一意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="66ff6-108">Each friend specifies a unique value for the **userID** element on the social network.</span></span> 
  
<span data-ttu-id="66ff6-109">フレンド **XML** の残りの要素には、自明の名前があります。</span><span class="sxs-lookup"><span data-stu-id="66ff6-109">The remaining elements of the **friends** XML have self-explanatory names.</span></span> <span data-ttu-id="66ff6-110">これらの要素の詳細については [、「XML for Friends」を参照してください](xml-for-friends.md)。</span><span class="sxs-lookup"><span data-stu-id="66ff6-110">For detailed description of these elements, see [XML for Friends](xml-for-friends.md).</span></span> 
  
## <a name="xml-example"></a><span data-ttu-id="66ff6-111">XML の例</span><span class="sxs-lookup"><span data-stu-id="66ff6-111">XML example</span></span>

<span data-ttu-id="66ff6-112">次の例は、 **ソーシャル ネットワーク上** の 2 人のフレンド XML を示しています。</span><span class="sxs-lookup"><span data-stu-id="66ff6-112">The following example shows the **friends** XML for two persons on the social network.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="66ff6-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="66ff6-113">See also</span></span>

- [<span data-ttu-id="66ff6-114">OSC プロバイダー XML の例</span><span class="sxs-lookup"><span data-stu-id="66ff6-114">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="66ff6-115">機能 XML の例</span><span class="sxs-lookup"><span data-stu-id="66ff6-115">Capabilities XML Example</span></span>](capabilities-xml-example.md) 
- [<span data-ttu-id="66ff6-116">アクティビティ フィード XML の例</span><span class="sxs-lookup"><span data-stu-id="66ff6-116">Activity Feed XML Example</span></span>](activity-feed-xml-example.md) 
- [<span data-ttu-id="66ff6-117">Outlookソーシャル コネクタ プロバイダー XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="66ff6-117">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

