---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: ソーシャル ネットワーク上のフレンドとして userID パラメーターによって識別されたユーザーを削除します。
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418436"
---
# <a name="isocialsessionunfollowperson"></a><span data-ttu-id="0f43d-103">ISocialSession::UnFollowPerson</span><span class="sxs-lookup"><span data-stu-id="0f43d-103">ISocialSession::UnFollowPerson</span></span>

<span data-ttu-id="0f43d-104">ソーシャル ネットワーク上のフレンドとして  _userID_ パラメーターによって識別されたユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="0f43d-104">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span> 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a><span data-ttu-id="0f43d-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f43d-105">Parameters</span></span>

<span data-ttu-id="0f43d-106">_userID_</span><span class="sxs-lookup"><span data-stu-id="0f43d-106">_userID_</span></span>
  
> <span data-ttu-id="0f43d-107">[in]ユーザーのソーシャル ネットワーク ユーザー ID を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="0f43d-107">[in] A string that contains a social network user ID for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0f43d-108">注釈</span><span class="sxs-lookup"><span data-stu-id="0f43d-108">Remarks</span></span>

<span data-ttu-id="0f43d-109">_userID パラメーター_ は、ソーシャル ネットワーク上のユーザーの有効なユーザー ID である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f43d-109">The  _userID_ parameter must be a valid user ID for the person on the social network.</span></span> 
  
<span data-ttu-id="0f43d-110">Outlook Social Connector (OSC) プロバイダーが機能の XML で **doNotFollowPerson** を true に設定している場合、渡されたユーザー ID がネットワーク上のユーザーと一致しない場合、プロバイダーは OSC_E_NOT_FOUND エラーを返す必要があります。 </span><span class="sxs-lookup"><span data-stu-id="0f43d-110">If the Outlook Social Connector (OSC) provider has set **doNotFollowPerson** as **true** in the XML for **capabilities**, the provider must return the OSC_E_NOT_FOUND error in the case that the user ID passed in does not match a user on the network.</span></span> <span data-ttu-id="0f43d-111">プロバイダーが **doNotFollowPerson** を機能で **false** に設定している場合、プロバイダーはエラーメッセージをOSC_E_FAILします。</span><span class="sxs-lookup"><span data-stu-id="0f43d-111">If the provider has set **doNotFollowPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> <span data-ttu-id="0f43d-112">エラー コードの詳細については、「[Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f43d-112">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0f43d-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f43d-113">See also</span></span>

- [<span data-ttu-id="0f43d-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0f43d-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

