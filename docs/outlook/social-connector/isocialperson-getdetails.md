---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: 名、名、プロファイル画像の URL など、人物の詳細を表す文字列を取得します。
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427333"
---
# <a name="isocialpersongetdetails"></a><span data-ttu-id="2e97c-103">ISocialPerson::GetDetails</span><span class="sxs-lookup"><span data-stu-id="2e97c-103">ISocialPerson::GetDetails</span></span>

<span data-ttu-id="2e97c-104">名、名、プロファイル画像の URL など、人物の詳細を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2e97c-104">Gets a string that represents details for the person, such as the first name, last name, and a URL to a profile picture.</span></span> 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a><span data-ttu-id="2e97c-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2e97c-105">Parameters</span></span>

<span data-ttu-id="2e97c-106">_details_</span><span class="sxs-lookup"><span data-stu-id="2e97c-106">_details_</span></span>
  
> <span data-ttu-id="2e97c-107">[out]ユーザーの詳細を表す XML 文字列値。</span><span class="sxs-lookup"><span data-stu-id="2e97c-107">[out] An XML string value that represents the details for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2e97c-108">注釈</span><span class="sxs-lookup"><span data-stu-id="2e97c-108">Remarks</span></span>

<span data-ttu-id="2e97c-109">返 _される詳細_ XML 文字列は、Outlook Social Connector (OSC) プロバイダーの機能拡張のスキーマで定義されている、ユーザーのスキーマ定義に準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e97c-109">The returned  _details_ XML string must comply with the schema definition for **person**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span>
  
<span data-ttu-id="2e97c-110">OSC プロバイダーがソーシャル ネットワーク上の友人のキャッシュまたはハイブリッド同期をサポートしている場合、OSC は **GetDetails** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2e97c-110">The OSC calls **GetDetails** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="2e97c-111">OSC は、ログオンしているユーザーのフレンドのアクティビティを最初に取得すると[、ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)を呼び出し、ログオンしているユーザーの既定の Outlook ストア内のソーシャル ネットワーク固有の連絡先フォルダーに友人の情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="2e97c-111">When the OSC initially gets friends' activities for the logged on user, it calls [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), and stores friends' information in a contacts folder specific to the social network, in the logged on user's default Outlook store.</span></span> <span data-ttu-id="2e97c-112">その後、キャッシュの更新間隔が経過していない限り **、OSC は GetFriendsAndColleagues** または **GetDetails** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2e97c-112">Subsequently the OSC does not call **GetFriendsAndColleagues** or **GetDetails** unless the refresh interval for the cache has expired.</span></span> <span data-ttu-id="2e97c-113">OSC が連絡先フォルダーに友人の情報をキャッシュする方法の詳細については、「友人とアクティビティの同期」 [を参照してください](synchronizing-friends-and-activities.md)。</span><span class="sxs-lookup"><span data-stu-id="2e97c-113">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2e97c-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="2e97c-114">See also</span></span>

- [<span data-ttu-id="2e97c-115">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2e97c-115">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

