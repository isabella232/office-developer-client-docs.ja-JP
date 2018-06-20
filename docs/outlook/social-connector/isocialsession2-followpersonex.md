---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: ソーシャル ネットワークにログオン中のユーザーのフレンドとして、emailAddresses パラメーターと displayName パラメーターで識別されるユーザーを追加します。
ms.openlocfilehash: 2f4df9afc4c769cce0502792373702c1281fcad7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804382"
---
# <a name="isocialsession2followpersonex"></a><span data-ttu-id="01847-103">ISocialSession2::FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="01847-103">ISocialSession2::FollowPersonEx</span></span>

<span data-ttu-id="01847-104">ソーシャル ネットワークにログオン中のユーザーのフレンドとして、 _emailAddresses_パラメーターと_displayName_パラメーターで識別されるユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="01847-104">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a><span data-ttu-id="01847-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="01847-105">Parameters</span></span>

<span data-ttu-id="01847-106">_emailAddresses_</span><span class="sxs-lookup"><span data-stu-id="01847-106">_emailAddresses_</span></span>
  
> <span data-ttu-id="01847-107">[in]ソーシャル ネットワーク上のユーザーの 1 つまたは複数の有効な SMTP アドレスを含む配列です。</span><span class="sxs-lookup"><span data-stu-id="01847-107">[in] An array that contains one or multiple valid SMTP addresses for a person on the social network.</span></span>
    
<span data-ttu-id="01847-108">_displayName_</span><span class="sxs-lookup"><span data-stu-id="01847-108">_displayName_</span></span>
  
> <span data-ttu-id="01847-109">[in]友人として追加するユーザーの表示名を含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="01847-109">[in] A string that contains the display name of the person to be added as a friend.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01847-110">備考</span><span class="sxs-lookup"><span data-stu-id="01847-110">Remarks</span></span>

<span data-ttu-id="01847-111">Outlook ソーシャル コネクタ (OSC) は、多くの場合よりも OSC プロバイダー、 **emailAddresses**パラメーターの配列内の SMTP アドレスの最初の要素は、プライマリ SMTP アドレスと仮定できます。</span><span class="sxs-lookup"><span data-stu-id="01847-111">If the Outlook Social Connector (OSC) provides more than on SMTP address in the array in the **emailAddresses** parameter, the OSC provider can assume the first element is the primary SMTP address.</span></span> 
  
<span data-ttu-id="01847-112">プロバイダーは**機能**XML で**は** **followPerson**要素を設定するには、ネットワーク上のユーザーが一致する_emailAddresses_の要素がない場合、プロバイダーは、OSC_E_NOT_FOUND エラーを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="01847-112">If the provider has set the **followPerson** element as **true** in the **capabilities** XML, and none of the elements for  _emailAddresses_ match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="01847-113">設定した場合、プロバイダー **followPerson** **false**として**の機能**で、プロバイダーは、OSC_E_FAIL エラーを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="01847-113">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> 
  
<span data-ttu-id="01847-114">**FollowPersonEx**メソッドが成功した場合、プロバイダー文字列を使用できます、 _displayName_パラメーターで SMTP アドレスを使用してユーザーをアドレス指定するのではなく、その後友人に確認の電子メールでユーザーに対応します。</span><span class="sxs-lookup"><span data-stu-id="01847-114">If the **FollowPersonEx** method succeeds, the provider can use the string in the  _displayName_ parameter to address the person in any subsequent friend-confirmation email, rather than addressing the person by the SMTP address.</span></span> <span data-ttu-id="01847-115">その一方で、プロバイダーがあります OSC の_displayName_パラメーターに空の文字列を渡すことを処理するために。</span><span class="sxs-lookup"><span data-stu-id="01847-115">On the other hand, the provider must be able to handle the OSC passing an empty string for the  _displayName_ parameter.</span></span> 
  
<span data-ttu-id="01847-116">プロバイダーは、 [ISocialSession2](isocialsession2iunknown.md)インターフェイスを実装するし、 **true**では、XML の機能として**followPerson**を設定するには、OSC は、 [ISocialSession::FollowPerson](isocialsession-followperson.md)の代わりに**FollowPersonEx**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="01847-116">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in the capabilities XML, the OSC calls **FollowPersonEx** instead of [ISocialSession::FollowPerson](isocialsession-followperson.md).</span></span> <span data-ttu-id="01847-117">プロバイダーは、 **true**として**followPerson**を設定しましたが、 **ISocialSession2**インターフェイスを実装しません、 **FollowPersonEx**が OSC_E_NOTIMPL のエラーを返す場合、OSC は**ISocialSession::FollowPerson**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="01847-117">If the provider has set **followPerson** as **true** but does not implement the **ISocialSession2** interface, or **FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC calls **ISocialSession::FollowPerson**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="01847-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="01847-118">See also</span></span>

- [<span data-ttu-id="01847-119">ISocialSession2: IUnknown</span><span class="sxs-lookup"><span data-stu-id="01847-119">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

