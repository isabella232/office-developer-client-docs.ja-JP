---
title: i入力 alsessiongetperson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: userID パラメーターに基づいて isocialperson インターフェイスを取得します。
ms.openlocfilehash: b54e39b3712fb57d89d03787f1e5fa0ff50ff84a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285331"
---
# <a name="isocialsessiongetperson"></a><span data-ttu-id="021d1-103">ISocialSession::GetPerson</span><span class="sxs-lookup"><span data-stu-id="021d1-103">ISocialSession::GetPerson</span></span>

<span data-ttu-id="021d1-104">_userID_パラメーターに基づいて[isocialperson](isocialpersoniunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="021d1-104">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a><span data-ttu-id="021d1-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="021d1-105">Parameters</span></span>

<span data-ttu-id="021d1-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="021d1-106">_userId_</span></span>
  
> <span data-ttu-id="021d1-107">順番個人のユーザー ID または SMTP アドレスを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="021d1-107">[in] A string that contains a user ID or SMTP address of a person.</span></span>
    
<span data-ttu-id="021d1-108">_result_</span><span class="sxs-lookup"><span data-stu-id="021d1-108">_result_</span></span>
  
> <span data-ttu-id="021d1-109">読み上げ**i社会 alperson**インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="021d1-109">[out] An **ISocialPerson** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="021d1-110">解説</span><span class="sxs-lookup"><span data-stu-id="021d1-110">Remarks</span></span>

<span data-ttu-id="021d1-111">_userID_パラメーターは、ユーザー ID または SMTP アドレスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="021d1-111">The  _userID_ parameter must be a user ID or SMTP address.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="021d1-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="021d1-112">See also</span></span>

- [<span data-ttu-id="021d1-113">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="021d1-113">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

