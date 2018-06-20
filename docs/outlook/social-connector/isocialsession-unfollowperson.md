---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: ソーシャル ネットワークの友人として、ユーザー Id のパラメーターで識別されるユーザーを削除します。
ms.openlocfilehash: 8b9a1e4f903e4bc805481b8679481103ea1ec82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804373"
---
# <a name="isocialsessionunfollowperson"></a><span data-ttu-id="57cc5-103">ISocialSession::UnFollowPerson</span><span class="sxs-lookup"><span data-stu-id="57cc5-103">ISocialSession::UnFollowPerson</span></span>

<span data-ttu-id="57cc5-104">ソーシャル ネットワークの友人として、_ユーザー Id_のパラメーターで識別されるユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="57cc5-104">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span> 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a><span data-ttu-id="57cc5-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="57cc5-105">Parameters</span></span>

<span data-ttu-id="57cc5-106">_ユーザー Id_</span><span class="sxs-lookup"><span data-stu-id="57cc5-106">_userID_</span></span>
  
> <span data-ttu-id="57cc5-107">[in]人のソーシャル ネットワークのユーザー ID を含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="57cc5-107">[in] A string that contains a social network user ID for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="57cc5-108">備考</span><span class="sxs-lookup"><span data-stu-id="57cc5-108">Remarks</span></span>

<span data-ttu-id="57cc5-109">_ユーザー Id_パラメーターは、ソーシャル ネットワーク上のユーザーの有効なユーザー ID である必要があります。</span><span class="sxs-lookup"><span data-stu-id="57cc5-109">The  _userID_ parameter must be a valid user ID for the person on the social network.</span></span> 
  
<span data-ttu-id="57cc5-110">Outlook ソーシャル コネクタ (OSC) プロバイダーは、**該当****機能**の XML で**doNotFollowPerson**を設定するには、プロバイダーは、ユーザーの ID が渡されますが、ネットワーク上のユーザーと一致しないことの場合は OSC_E_NOT_FOUND エラーを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="57cc5-110">If the Outlook Social Connector (OSC) provider has set **doNotFollowPerson** as **true** in the XML for **capabilities**, the provider must return the OSC_E_NOT_FOUND error in the case that the user ID passed in does not match a user on the network.</span></span> <span data-ttu-id="57cc5-111">設定した場合、プロバイダー **doNotFollowPerson** **false**として**の機能**で、プロバイダーは、OSC_E_FAIL エラーを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="57cc5-111">If the provider has set **doNotFollowPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> <span data-ttu-id="57cc5-112">エラー コードの詳細については、 [Outlook ソーシャル コネクタ プロバイダーのエラー コード](outlook-social-connector-provider-error-codes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="57cc5-112">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="57cc5-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="57cc5-113">See also</span></span>

- [<span data-ttu-id="57cc5-114">ISocialSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="57cc5-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

