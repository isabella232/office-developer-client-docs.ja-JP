---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: ソーシャル ネットワークにログオン中のユーザーのフレンドとして、emailAddress パラメーターで識別されるユーザーを追加します。
ms.openlocfilehash: 6dc289801c99f2f3bf1647e9c98c072d2f53d066
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804364"
---
# <a name="isocialsessionfollowperson"></a><span data-ttu-id="cf775-103">ISocialSession::FollowPerson</span><span class="sxs-lookup"><span data-stu-id="cf775-103">ISocialSession::FollowPerson</span></span>

<span data-ttu-id="cf775-104">ソーシャル ネットワークにログオン中のユーザーのフレンドとして、 _emailAddress_パラメーターで識別されるユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="cf775-104">Adds the person identified by the  _emailAddress_ parameter as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a><span data-ttu-id="cf775-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="cf775-105">Parameters</span></span>

<span data-ttu-id="cf775-106">_emailAddress_</span><span class="sxs-lookup"><span data-stu-id="cf775-106">_emailAddress_</span></span>
  
> <span data-ttu-id="cf775-107">[in]人物の電子メール アドレスを含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="cf775-107">[in] A string that contains an email address of a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cf775-108">備考</span><span class="sxs-lookup"><span data-stu-id="cf775-108">Remarks</span></span>

<span data-ttu-id="cf775-109">_EmailAddress_パラメーターは、有効な SMTP アドレスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf775-109">The  _emailAddress_ parameter must be a valid SMTP address.</span></span> <span data-ttu-id="cf775-110">プロバイダーは、OSC_E_NOT_FOUND を返す必要があります、Outlook ソーシャル コネクタ (OSC) プロバイダーが設定して、 **followPerson**メソッド**は true**として**機能**、 _emailAddress_の引数は、ネットワーク上のユーザーと一致しない場合は、エラーです。</span><span class="sxs-lookup"><span data-stu-id="cf775-110">If the Outlook Social Connector (OSC) provider has set the **followPerson** method as **true** in **capabilities**, and the argument for  _emailAddress_ does not match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="cf775-111">設定した場合、プロバイダー **followPerson** **false**として**の機能**で、プロバイダーは、OSC_E_FAIL エラーを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf775-111">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span>
  
<span data-ttu-id="cf775-112">OSC が**ISocialSession::FollowPerson の代わりに[ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md)を呼び出す場合は、プロバイダーでは、 [ISocialSession2](isocialsession2iunknown.md)インターフェイスを実装して、**機能**で**は** **followPerson**に設定が、**.</span><span class="sxs-lookup"><span data-stu-id="cf775-112">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in **capabilities**, the OSC will call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of **ISocialSession::FollowPerson**.</span></span> <span data-ttu-id="cf775-113">プロバイダーに**が設定されている限りに、OSC が**ISocialSession::FollowPerson**を呼び出す場合、プロバイダー インターフェイスを実装しません、 **ISocialSession2** 、または**ISocialSession2::FollowPersonEx**には、OSC_E_NOTIMPL エラーが返されます、followPerson**として**真**に**機能**します。</span><span class="sxs-lookup"><span data-stu-id="cf775-113">If the provider does not implement the **ISocialSession2** interface, or **ISocialSession2::FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC will call **ISocialSession::FollowPerson** as long as the provider has set **followPerson** as **true** in **capabilities**.</span></span> <span data-ttu-id="cf775-114">エラー コードの詳細については、 [Outlook ソーシャル コネクタ プロバイダーのエラー コード](outlook-social-connector-provider-error-codes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cf775-114">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
<span data-ttu-id="cf775-115">かどうか**ISocalSession::FollowPerson**または**ISocialSession2::FollowPersonEx**を実装するにする必要があるかどうかと**ISocialSession2**、内の他のメソッドが、プロバイダーに必要があるかどうかを決定する際に、_を使用することができます。djsplayName_ **FollowPersonEx**内のパラメーターです。</span><span class="sxs-lookup"><span data-stu-id="cf775-115">In deciding whether to implement **ISocalSession::FollowPerson** or **ISocialSession2::FollowPersonEx**, you should consider whether your provider needs the other methods in **ISocialSession2**, and whether you can use the  _djsplayName_ parameter in **FollowPersonEx**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf775-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf775-116">See also</span></span>

- [<span data-ttu-id="cf775-117">ISocialSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf775-117">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

