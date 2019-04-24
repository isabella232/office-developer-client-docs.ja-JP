---
title: i社会 al個人 getdetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: 名、姓、プロファイル画像への URL など、個人の詳細を表す文字列を取得します。
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286144"
---
# <a name="isocialpersongetdetails"></a><span data-ttu-id="b3bdf-103">ISocialPerson::GetDetails</span><span class="sxs-lookup"><span data-stu-id="b3bdf-103">ISocialPerson::GetDetails</span></span>

<span data-ttu-id="b3bdf-104">名、姓、プロファイル画像への URL など、個人の詳細を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="b3bdf-104">Gets a string that represents details for the person, such as the first name, last name, and a URL to a profile picture.</span></span> 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a><span data-ttu-id="b3bdf-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b3bdf-105">Parameters</span></span>

<span data-ttu-id="b3bdf-106">_details_</span><span class="sxs-lookup"><span data-stu-id="b3bdf-106">_details_</span></span>
  
> <span data-ttu-id="b3bdf-107">読み上げ個人の詳細を表す XML 文字列型 (string) の値。</span><span class="sxs-lookup"><span data-stu-id="b3bdf-107">[out] An XML string value that represents the details for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b3bdf-108">解説</span><span class="sxs-lookup"><span data-stu-id="b3bdf-108">Remarks</span></span>

<span data-ttu-id="b3bdf-109">返される_詳細_XML 文字列は、Outlook Social Connector (.osc) プロバイダー拡張機能のスキーマで定義されているように、 **person**のスキーマ定義に準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3bdf-109">The returned  _details_ XML string must comply with the schema definition for **person**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span>
  
<span data-ttu-id="b3bdf-110">.osc プロバイダーがソーシャルネットワーク上で友人のキャッシュまたはハイブリッド同期をサポートしている場合、.osc は**getdetails**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b3bdf-110">The OSC calls **GetDetails** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="b3bdf-111">.osc が、ログオンしているユーザーのフレンドのアクティビティを最初に取得するときに、 [iGetFriendsAndColleagues alperson:::](isocialperson-getfriendsandcolleagues.md)を呼び出し、ソーシャルネットワーク固有の連絡先フォルダーに友人の情報を格納します。これには、ログオンユーザーの既定の Outlook ストアが含まれます。.</span><span class="sxs-lookup"><span data-stu-id="b3bdf-111">When the OSC initially gets friends' activities for the logged on user, it calls [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), and stores friends' information in a contacts folder specific to the social network, in the logged on user's default Outlook store.</span></span> <span data-ttu-id="b3bdf-112">その後、.osc は、キャッシュの更新間隔が経過していない限り、 **GetFriendsAndColleagues**または**getdetails**を呼び出しません。</span><span class="sxs-lookup"><span data-stu-id="b3bdf-112">Subsequently the OSC does not call **GetFriendsAndColleagues** or **GetDetails** unless the refresh interval for the cache has expired.</span></span> <span data-ttu-id="b3bdf-113">.osc が連絡先フォルダー内のフレンド情報をキャッシュする方法の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3bdf-113">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b3bdf-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="b3bdf-114">See also</span></span>

- [<span data-ttu-id="b3bdf-115">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b3bdf-115">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

