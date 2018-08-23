---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: プロフィールの画像に、名、姓、名、URL など、個人の詳細情報を表す文字列を取得します。
ms.openlocfilehash: 158ce9b5c6a97ffff0325427ed07c74f518941d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804339"
---
# <a name="isocialpersongetdetails"></a><span data-ttu-id="021b0-103">ISocialPerson::GetDetails</span><span class="sxs-lookup"><span data-stu-id="021b0-103">ISocialPerson::GetDetails</span></span>

<span data-ttu-id="021b0-104">プロフィールの画像に、名、姓、名、URL など、個人の詳細情報を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="021b0-104">Gets a string that represents details for the person, such as the first name, last name, and a URL to a profile picture.</span></span> 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a><span data-ttu-id="021b0-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="021b0-105">Parameters</span></span>

<span data-ttu-id="021b0-106">_詳細情報_</span><span class="sxs-lookup"><span data-stu-id="021b0-106">_details_</span></span>
  
> <span data-ttu-id="021b0-107">[out]個人の詳細情報を表す XML 文字列値。</span><span class="sxs-lookup"><span data-stu-id="021b0-107">[out] An XML string value that represents the details for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="021b0-108">注釈</span><span class="sxs-lookup"><span data-stu-id="021b0-108">Remarks</span></span>

<span data-ttu-id="021b0-109">返される_詳細情報_の XML 文字列は、Outlook ソーシャル コネクタ (OSC) プロバイダーの機能拡張のスキーマで定義されている**人**の場合は、スキーマ定義に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="021b0-109">The returned  _details_ XML string must comply with the schema definition for **person**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span>
  
<span data-ttu-id="021b0-110">OSC は、ソーシャル ネットワーク上の**GetDetails** OSC プロバイダーをサポートしていますがキャッシュされている場合、またはハイブリッドの同期の友人を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="021b0-110">The OSC calls **GetDetails** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="021b0-111">OSC は、最初にログオンしたユーザーの友人の活動を取得、それは[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)と友人の情報をソーシャル ネットワークにログオンしたユーザーの既定の Outlook ストアに特定の連絡先フォルダーに格納.</span><span class="sxs-lookup"><span data-stu-id="021b0-111">When the OSC initially gets friends' activities for the logged on user, it calls [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), and stores friends' information in a contacts folder specific to the social network, in the logged on user's default Outlook store.</span></span> <span data-ttu-id="021b0-112">その後、OSC を呼び出しません**GetFriendsAndColleagues**または**GetDetails**キャッシュの更新間隔の有効期限が切れていない限り。</span><span class="sxs-lookup"><span data-stu-id="021b0-112">Subsequently the OSC does not call **GetFriendsAndColleagues** or **GetDetails** unless the refresh interval for the cache has expired.</span></span> <span data-ttu-id="021b0-113">OSC が連絡先フォルダー内の友人の情報をキャッシュする方法の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="021b0-113">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="021b0-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="021b0-114">See also</span></span>

- [<span data-ttu-id="021b0-115">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="021b0-115">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

