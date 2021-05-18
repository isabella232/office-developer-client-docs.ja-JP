---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: emailAddress パラメーターで識別されたユーザーを、ソーシャル ネットワーク上のログオンユーザーのフレンドとして追加します。
ms.openlocfilehash: 849085bd40788039a96ac159fd76a5e252395916
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423259"
---
# <a name="isocialsessionfollowperson"></a><span data-ttu-id="04b14-103">ISocialSession::FollowPerson</span><span class="sxs-lookup"><span data-stu-id="04b14-103">ISocialSession::FollowPerson</span></span>

<span data-ttu-id="04b14-104">_emailAddress_ パラメーターで識別されたユーザーを、ソーシャル ネットワーク上のログオンユーザーのフレンドとして追加します。</span><span class="sxs-lookup"><span data-stu-id="04b14-104">Adds the person identified by the  _emailAddress_ parameter as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a><span data-ttu-id="04b14-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04b14-105">Parameters</span></span>

<span data-ttu-id="04b14-106">_emailAddress_</span><span class="sxs-lookup"><span data-stu-id="04b14-106">_emailAddress_</span></span>
  
> <span data-ttu-id="04b14-107">[in]ユーザーの電子メール アドレスを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="04b14-107">[in] A string that contains an email address of a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="04b14-108">注釈</span><span class="sxs-lookup"><span data-stu-id="04b14-108">Remarks</span></span>

<span data-ttu-id="04b14-109">_emailAddress パラメーター_ は、有効な SMTP アドレスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="04b14-109">The  _emailAddress_ parameter must be a valid SMTP address.</span></span> <span data-ttu-id="04b14-110">Outlook Social Connector (OSC) プロバイダーが **followPerson** メソッドを機能でtrue に設定し _、emailAddress_ の引数がネットワーク上のユーザーと一致しない場合、プロバイダーは OSC_E_NOT_FOUND エラーを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="04b14-110">If the Outlook Social Connector (OSC) provider has set the **followPerson** method as **true** in **capabilities**, and the argument for  _emailAddress_ does not match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="04b14-111">プロバイダーが **followPerson** を機能で **false** に設定している場合、プロバイダーはエラー メッセージをOSC_E_FAILします。</span><span class="sxs-lookup"><span data-stu-id="04b14-111">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span>
  
<span data-ttu-id="04b14-112">プロバイダーが [ISocialSession2](isocialsession2iunknown.md)インターフェイスを実装し **、followPerson** を機能に **true** に設定している場合、OSC は **ISocialSession::FollowPerson ではなく ISocialSession2::FollowPersonEx** を呼び出します。 [](isocialsession2-followpersonex.md)</span><span class="sxs-lookup"><span data-stu-id="04b14-112">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in **capabilities**, the OSC will call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of **ISocialSession::FollowPerson**.</span></span> <span data-ttu-id="04b14-113">プロバイダーが **ISocialSession2** インターフェイスを実装しない場合、または **ISocialSession2::FollowPersonEx** が OSC_E_NOTIMPL エラーを返す場合、プロバイダーが **followPerson** を機能で true に設定している限り、OSC は **ISocialSession::FollowPerson** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="04b14-113">If the provider does not implement the **ISocialSession2** interface, or **ISocialSession2::FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC will call **ISocialSession::FollowPerson** as long as the provider has set **followPerson** as **true** in **capabilities**.</span></span> <span data-ttu-id="04b14-114">エラー コードの詳細については、「[Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="04b14-114">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
<span data-ttu-id="04b14-115">**ISocalSession:::FollowPerson** または **ISocialSession2::FollowPersonEx** を実装するかどうかを決定する際には、プロバイダーが **ISocialSession2** で他のメソッドを必要とするかどうか、**および FollowPersonEx** で _djsplayName_ パラメーターを使用できるかどうかを検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04b14-115">In deciding whether to implement **ISocalSession::FollowPerson** or **ISocialSession2::FollowPersonEx**, you should consider whether your provider needs the other methods in **ISocialSession2**, and whether you can use the  _djsplayName_ parameter in **FollowPersonEx**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="04b14-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="04b14-116">See also</span></span>

- [<span data-ttu-id="04b14-117">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="04b14-117">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

