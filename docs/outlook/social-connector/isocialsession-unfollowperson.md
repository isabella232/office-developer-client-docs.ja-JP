---
title: iの入力
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: userID パラメーターで指定された人物をソーシャルネットワーク上のフレンドとして削除します。
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418436"
---
# <a name="isocialsessionunfollowperson"></a><span data-ttu-id="8911d-103">ISocialSession::UnFollowPerson</span><span class="sxs-lookup"><span data-stu-id="8911d-103">ISocialSession::UnFollowPerson</span></span>

<span data-ttu-id="8911d-104">_userID_パラメーターで指定された人物をソーシャルネットワーク上のフレンドとして削除します。</span><span class="sxs-lookup"><span data-stu-id="8911d-104">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span> 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a><span data-ttu-id="8911d-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8911d-105">Parameters</span></span>

<span data-ttu-id="8911d-106">_userID_</span><span class="sxs-lookup"><span data-stu-id="8911d-106">_userID_</span></span>
  
> <span data-ttu-id="8911d-107">順番ユーザーのソーシャルネットワークユーザー ID を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="8911d-107">[in] A string that contains a social network user ID for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8911d-108">注釈</span><span class="sxs-lookup"><span data-stu-id="8911d-108">Remarks</span></span>

<span data-ttu-id="8911d-109">_userID_パラメーターには、ソーシャルネットワーク上のユーザーの有効なユーザー ID を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8911d-109">The  _userID_ parameter must be a valid user ID for the person on the social network.</span></span> 
  
<span data-ttu-id="8911d-110">Outlook Social Connector (.osc) プロバイダーが、**機能**の\*\*\*\* XML で [ **true** ] に設定されている場合、渡されたユーザー ID がネットワーク上のユーザーと一致しない場合、プロバイダーは OSC_E_NOT_FOUND エラーを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8911d-110">If the Outlook Social Connector (OSC) provider has set **doNotFollowPerson** as **true** in the XML for **capabilities**, the provider must return the OSC_E_NOT_FOUND error in the case that the user ID passed in does not match a user on the network.</span></span> <span data-ttu-id="8911d-111">プロバイダーが [**機能**] \*\*\*\* の値を**false**に設定している場合、プロバイダーは OSC_E_FAIL エラーを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8911d-111">If the provider has set **doNotFollowPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> <span data-ttu-id="8911d-112">エラー コードの詳細については、「[Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8911d-112">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8911d-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="8911d-113">See also</span></span>

- [<span data-ttu-id="8911d-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8911d-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

