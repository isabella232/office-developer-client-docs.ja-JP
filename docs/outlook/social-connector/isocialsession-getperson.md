---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: ユーザー Id のパラメーターに基づいて、ISocialPerson インターフェイスを取得します。
ms.openlocfilehash: 5769f4c41bb97f45ab722f1b3a3febe24c8a7ab2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804362"
---
# <a name="isocialsessiongetperson"></a><span data-ttu-id="e9814-103">ISocialSession::GetPerson</span><span class="sxs-lookup"><span data-stu-id="e9814-103">ISocialSession::GetPerson</span></span>

<span data-ttu-id="e9814-104">_ユーザー Id_のパラメーターに基づいて、 [ISocialPerson](isocialpersoniunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="e9814-104">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a><span data-ttu-id="e9814-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="e9814-105">Parameters</span></span>

<span data-ttu-id="e9814-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="e9814-106">_userId_</span></span>
  
> <span data-ttu-id="e9814-107">[in]人のユーザー ID、または SMTP アドレスを含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="e9814-107">[in] A string that contains a user ID or SMTP address of a person.</span></span>
    
<span data-ttu-id="e9814-108">_result_</span><span class="sxs-lookup"><span data-stu-id="e9814-108">_result_</span></span>
  
> <span data-ttu-id="e9814-109">[out]**ISocialPerson**インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="e9814-109">[out] An **ISocialPerson** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e9814-110">備考</span><span class="sxs-lookup"><span data-stu-id="e9814-110">Remarks</span></span>

<span data-ttu-id="e9814-111">_ユーザー Id_パラメーターは、ユーザーの ID または SMTP アドレスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9814-111">The  _userID_ parameter must be a user ID or SMTP address.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e9814-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9814-112">See also</span></span>

- [<span data-ttu-id="e9814-113">ISocialSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e9814-113">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

