---
title: 友だち XML の例
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83afbdef-4f12-4673-a0c1-bbf86274558f
description: XML の例をこのトピックでは、ISocialPerson::GetFriendsAndColleagues メソッドが呼び出された後に、Outlook ソーシャル コネクタ (OSC) が返されるフレンド XML 文字列です。 例は、人の要素で区切られたそれぞれの 2 つの友人、友人の XML を示します。 各友人は、ソーシャル ネットワーク上のユーザー Id の要素に一意の値を指定します。
ms.openlocfilehash: 6944213e9483042862fa4cefd8420e39ade9139f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804326"
---
# <a name="friends-xml-example"></a><span data-ttu-id="a973e-105">友だち XML の例</span><span class="sxs-lookup"><span data-stu-id="a973e-105">Friends XML example</span></span>

<span data-ttu-id="a973e-106">XML の例をこのトピックでは、 [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)メソッドが呼び出された後に、Outlook ソーシャル コネクタ (OSC) が返されるフレンド XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="a973e-106">The XML example in this topic is a friend XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method.</span></span> <span data-ttu-id="a973e-107">例は、**人**の要素で区切られた各、2 つの友人の**友人**の XML を示します。</span><span class="sxs-lookup"><span data-stu-id="a973e-107">The example shows the **friends** XML for two friends, each delimited by the **person** element.</span></span> <span data-ttu-id="a973e-108">各友人は、ソーシャル ネットワーク上の**ユーザー Id**の要素に一意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="a973e-108">Each friend specifies a unique value for the **userID** element on the social network.</span></span> 
  
<span data-ttu-id="a973e-109">XML、**友人**の残りの要素では、わかりやすいものの名前を持ちます。</span><span class="sxs-lookup"><span data-stu-id="a973e-109">The remaining elements of the **friends** XML have self-explanatory names.</span></span> <span data-ttu-id="a973e-110">これらの要素の詳細については、[友人の XML](xml-for-friends.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a973e-110">For detailed description of these elements, see [XML for Friends](xml-for-friends.md).</span></span> 
  
## <a name="xml-example"></a><span data-ttu-id="a973e-111">XML の例</span><span class="sxs-lookup"><span data-stu-id="a973e-111">XML example</span></span>

<span data-ttu-id="a973e-112">次の例では、ソーシャル ネットワーク上の二人の**友人**の XML を示しています。</span><span class="sxs-lookup"><span data-stu-id="a973e-112">The following example shows the **friends** XML for two persons on the social network.</span></span> 
  
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
    <webProfilePage>http://contoso.com/melissa</webProfilePage>
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
    <webProfilePage>http://contoso.com/michael</webProfilePage>
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

## <a name="see-also"></a><span data-ttu-id="a973e-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="a973e-113">See also</span></span>

- [<span data-ttu-id="a973e-114">OSC プロバイダーの XML の例</span><span class="sxs-lookup"><span data-stu-id="a973e-114">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="a973e-115">機能の XML の例</span><span class="sxs-lookup"><span data-stu-id="a973e-115">Capabilities XML Example</span></span>](capabilities-xml-example.md) 
- [<span data-ttu-id="a973e-116">アクティビティ フィードの XML の例</span><span class="sxs-lookup"><span data-stu-id="a973e-116">Activity Feed XML Example</span></span>](activity-feed-xml-example.md) 
- [<span data-ttu-id="a973e-117">Outlook ソーシャル コネクタ プロバイダーの XML スキーマ</span><span class="sxs-lookup"><span data-stu-id="a973e-117">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

