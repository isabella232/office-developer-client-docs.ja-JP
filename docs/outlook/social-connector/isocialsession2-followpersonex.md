---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: emailaddresses および displayName パラメーターで指定された人物を、ソーシャルネットワーク上のログオンユーザーのフレンドとして追加します。
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429832"
---
# <a name="isocialsession2followpersonex"></a><span data-ttu-id="ecfb0-103">ISocialSession2::FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="ecfb0-103">ISocialSession2::FollowPersonEx</span></span>

<span data-ttu-id="ecfb0-104">_emailaddresses_および_displayName_パラメーターで指定された人物を、ソーシャルネットワーク上のログオンユーザーのフレンドとして追加します。</span><span class="sxs-lookup"><span data-stu-id="ecfb0-104">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a><span data-ttu-id="ecfb0-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ecfb0-105">Parameters</span></span>

<span data-ttu-id="ecfb0-106">_emailAddresses_</span><span class="sxs-lookup"><span data-stu-id="ecfb0-106">_emailAddresses_</span></span>
  
> <span data-ttu-id="ecfb0-107">順番ソーシャルネットワーク上の個人の1つまたは複数の有効な SMTP アドレスが格納された配列。</span><span class="sxs-lookup"><span data-stu-id="ecfb0-107">[in] An array that contains one or multiple valid SMTP addresses for a person on the social network.</span></span>
    
<span data-ttu-id="ecfb0-108">_displayName_</span><span class="sxs-lookup"><span data-stu-id="ecfb0-108">_displayName_</span></span>
  
> <span data-ttu-id="ecfb0-109">順番フレンドとして追加する人物の表示名を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="ecfb0-109">[in] A string that contains the display name of the person to be added as a friend.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ecfb0-110">注釈</span><span class="sxs-lookup"><span data-stu-id="ecfb0-110">Remarks</span></span>

<span data-ttu-id="ecfb0-111">Outlook Social Connector (.osc) が**emailaddresses**パラメーターの配列内の SMTP アドレスよりも多い場合、.osc プロバイダーは最初の要素がプライマリ SMTP アドレスであると見なすことができます。</span><span class="sxs-lookup"><span data-stu-id="ecfb0-111">If the Outlook Social Connector (OSC) provides more than on SMTP address in the array in the **emailAddresses** parameter, the OSC provider can assume the first element is the primary SMTP address.</span></span> 
  
<span data-ttu-id="ecfb0-112">プロバイダーが [**機能**] XML \*\*\*\* で [ **true** ] に設定されている場合、_電子メールアドレス_のどの要素もネットワーク上のユーザーと一致しない場合、プロバイダーは OSC_E_NOT_FOUND エラーを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecfb0-112">If the provider has set the **followPerson** element as **true** in the **capabilities** XML, and none of the elements for  _emailAddresses_ match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="ecfb0-113">プロバイダーが**権限**で OSC_E_FAIL \*\*\*\* を**false**として設定している場合、プロバイダーはエラーを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecfb0-113">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> 
  
<span data-ttu-id="ecfb0-114">このメソッド\*\*\*\* が正常に実行された場合、プロバイダーは_displayName_パラメーターの文字列を使用して、SMTP アドレスでその人物にアドレス指定するのではなく、その人物に対して任意のフレンドリな確認メールを送信することができます。</span><span class="sxs-lookup"><span data-stu-id="ecfb0-114">If the **FollowPersonEx** method succeeds, the provider can use the string in the  _displayName_ parameter to address the person in any subsequent friend-confirmation email, rather than addressing the person by the SMTP address.</span></span> <span data-ttu-id="ecfb0-115">一方、プロバイダーは、 _displayName_パラメーターに空の文字列を渡して、.osc を処理できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecfb0-115">On the other hand, the provider must be able to handle the OSC passing an empty string for the  _displayName_ parameter.</span></span> 
  
<span data-ttu-id="ecfb0-116">プロバイダーが[ISocialSession2](isocialsession2iunknown.md)インターフェイスを実装していて\*\*\*\* 、capabilities XML に**true**として設定されて\*\*\*\* いる場合、.osc は、 [i alsession::](isocialsession-followperson.md)という形式ではなく、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="ecfb0-116">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in the capabilities XML, the OSC calls **FollowPersonEx** instead of [ISocialSession::FollowPerson](isocialsession-followperson.md).</span></span> <span data-ttu-id="ecfb0-117">プロバイダーが**true**とし\*\*\*\* て**ISocialSession2**インターフェイスを実装していない場合、または\*\*\*\* OSC_E_NOTIMPL エラーが発生した場合、.osc は**i alsession::** という名前を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ecfb0-117">If the provider has set **followPerson** as **true** but does not implement the **ISocialSession2** interface, or **FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC calls **ISocialSession::FollowPerson**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ecfb0-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="ecfb0-118">See also</span></span>

- [<span data-ttu-id="ecfb0-119">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ecfb0-119">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

