---
title: i社会 alsessionん
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: ソーシャルネットワークにログオンしているユーザーのフレンドとして、emailAddress パラメーターによって識別された人物を追加します。
ms.openlocfilehash: 849085bd40788039a96ac159fd76a5e252395916
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423259"
---
# <a name="isocialsessionfollowperson"></a><span data-ttu-id="46926-103">ISocialSession::FollowPerson</span><span class="sxs-lookup"><span data-stu-id="46926-103">ISocialSession::FollowPerson</span></span>

<span data-ttu-id="46926-104">ソーシャルネットワークにログオンしているユーザーのフレンドとして、 _emailAddress_パラメーターによって識別された人物を追加します。</span><span class="sxs-lookup"><span data-stu-id="46926-104">Adds the person identified by the  _emailAddress_ parameter as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a><span data-ttu-id="46926-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="46926-105">Parameters</span></span>

<span data-ttu-id="46926-106">_emailAddress_</span><span class="sxs-lookup"><span data-stu-id="46926-106">_emailAddress_</span></span>
  
> <span data-ttu-id="46926-107">順番個人の電子メールアドレスを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="46926-107">[in] A string that contains an email address of a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="46926-108">注釈</span><span class="sxs-lookup"><span data-stu-id="46926-108">Remarks</span></span>

<span data-ttu-id="46926-109">_emailAddress_パラメーターは、有効な SMTP アドレスであることが必要です。</span><span class="sxs-lookup"><span data-stu-id="46926-109">The  _emailAddress_ parameter must be a valid SMTP address.</span></span> <span data-ttu-id="46926-110">Outlook Social Connector (.osc) プロバイダーが、**機能**では\*\*\*\* 、 _emailAddress_の引数が**true**として設定されており、その引数がネットワーク上のユーザーと一致しない場合、プロバイダーは OSC_E_NOT_FOUND を返す必要があります。エラー.</span><span class="sxs-lookup"><span data-stu-id="46926-110">If the Outlook Social Connector (OSC) provider has set the **followPerson** method as **true** in **capabilities**, and the argument for  _emailAddress_ does not match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="46926-111">プロバイダーが**権限**で OSC_E_FAIL \*\*\*\* を**false**として設定している場合、プロバイダーはエラーを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="46926-111">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span>
  
<span data-ttu-id="46926-112">プロバイダーが[ISocialSession2](isocialsession2iunknown.md)インターフェイスを実装していて\*\*\*\* 、**機能**に**true**として ISocialSession2 が設定されている場合、.osc は、i alsession:::/の代わりに、 [::](isocialsession2-followpersonex.md)のようにします。 \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="46926-112">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in **capabilities**, the OSC will call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of **ISocialSession::FollowPerson**.</span></span> <span data-ttu-id="46926-113">プロバイダーが**ISocialSession2**インターフェイスを実装していない場合、または**ISocialSession2::** を返します。 OSC_E_NOTIMPL エラーを返します。この場合、.osc は、プロバイダーが設定\*\*\*\* **されている限り、i alsession:: という名前を呼び出します。\*\*\*\*機能**につい\*\*\*\* ての概要</span><span class="sxs-lookup"><span data-stu-id="46926-113">If the provider does not implement the **ISocialSession2** interface, or **ISocialSession2::FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC will call **ISocialSession::FollowPerson** as long as the provider has set **followPerson** as **true** in **capabilities**.</span></span> <span data-ttu-id="46926-114">エラー コードの詳細については、「[Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="46926-114">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
<span data-ttu-id="46926-115">**isocalsession::** **ISocialSession2::** を実装するかどうかを決定するには、プロバイダーが**ISocialSession2**内の他のメソッドを必要とするかどうか、およびその方法を使用_できるかどうかを検討する必要があります。djsplayName_パラメーターを\*\*\*\* 指定します。</span><span class="sxs-lookup"><span data-stu-id="46926-115">In deciding whether to implement **ISocalSession::FollowPerson** or **ISocialSession2::FollowPersonEx**, you should consider whether your provider needs the other methods in **ISocialSession2**, and whether you can use the  _djsplayName_ parameter in **FollowPersonEx**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="46926-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="46926-116">See also</span></span>

- [<span data-ttu-id="46926-117">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="46926-117">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

