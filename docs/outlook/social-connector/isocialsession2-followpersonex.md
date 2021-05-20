---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: emailAddresses パラメーターと displayName パラメーターで識別されるユーザーを、ソーシャル ネットワーク上のログオンユーザーのフレンドとして追加します。
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429832"
---
# <a name="isocialsession2followpersonex"></a><span data-ttu-id="a9265-103">ISocialSession2::FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="a9265-103">ISocialSession2::FollowPersonEx</span></span>

<span data-ttu-id="a9265-104">_emailAddresses_ パラメーターと _displayName_ パラメーターで識別されるユーザーを、ソーシャル ネットワーク上のログオンユーザーのフレンドとして追加します。</span><span class="sxs-lookup"><span data-stu-id="a9265-104">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a><span data-ttu-id="a9265-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a9265-105">Parameters</span></span>

<span data-ttu-id="a9265-106">_emailAddresses_</span><span class="sxs-lookup"><span data-stu-id="a9265-106">_emailAddresses_</span></span>
  
> <span data-ttu-id="a9265-107">[in]ソーシャル ネットワーク上のユーザーの有効な SMTP アドレスを 1 つ以上含む配列。</span><span class="sxs-lookup"><span data-stu-id="a9265-107">[in] An array that contains one or multiple valid SMTP addresses for a person on the social network.</span></span>
    
<span data-ttu-id="a9265-108">_displayName_</span><span class="sxs-lookup"><span data-stu-id="a9265-108">_displayName_</span></span>
  
> <span data-ttu-id="a9265-109">[in]フレンドとして追加するユーザーの表示名を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="a9265-109">[in] A string that contains the display name of the person to be added as a friend.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a9265-110">注釈</span><span class="sxs-lookup"><span data-stu-id="a9265-110">Remarks</span></span>

<span data-ttu-id="a9265-111">Outlook ソーシャル コネクタ (OSC) が **emailAddresses** パラメーターの配列内の SMTP アドレスよりも多くを提供する場合、OSC プロバイダーは、最初の要素がプライマリ SMTP アドレスと見なされます。</span><span class="sxs-lookup"><span data-stu-id="a9265-111">If the Outlook Social Connector (OSC) provides more than on SMTP address in the array in the **emailAddresses** parameter, the OSC provider can assume the first element is the primary SMTP address.</span></span> 
  
<span data-ttu-id="a9265-112">プロバイダーが、機能 **XML** で **followPerson** 要素を true に設定し _、emailAddresses_ の要素のいずれもネットワーク上のユーザーと一致しない場合、プロバイダーは OSC_E_NOT_FOUND エラーを返す必要があります。 </span><span class="sxs-lookup"><span data-stu-id="a9265-112">If the provider has set the **followPerson** element as **true** in the **capabilities** XML, and none of the elements for  _emailAddresses_ match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="a9265-113">プロバイダーが **followPerson** を機能で **false** に設定している場合、プロバイダーはエラー メッセージをOSC_E_FAILします。</span><span class="sxs-lookup"><span data-stu-id="a9265-113">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> 
  
<span data-ttu-id="a9265-114">**FollowPersonEx** メソッドが成功した場合、プロバイダーは _displayName_ パラメーターの文字列を使用して、そのユーザーに SMTP アドレスでアドレス指定するのではなく、後続のフレンド確認メールのユーザーにアドレスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="a9265-114">If the **FollowPersonEx** method succeeds, the provider can use the string in the  _displayName_ parameter to address the person in any subsequent friend-confirmation email, rather than addressing the person by the SMTP address.</span></span> <span data-ttu-id="a9265-115">一方、プロバイダーは displayName パラメーターに空の文字列を渡す OSC を  _処理できる必要_ があります。</span><span class="sxs-lookup"><span data-stu-id="a9265-115">On the other hand, the provider must be able to handle the OSC passing an empty string for the  _displayName_ parameter.</span></span> 
  
<span data-ttu-id="a9265-116">プロバイダーが [ISocialSession2](isocialsession2iunknown.md)インターフェイスを実装し、機能 XML で **followPerson** を **true** に設定している場合、OSC は [ISocialSession::FollowPerson](isocialsession-followperson.md)の代わりに **FollowPersonEx** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a9265-116">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in the capabilities XML, the OSC calls **FollowPersonEx** instead of [ISocialSession::FollowPerson](isocialsession-followperson.md).</span></span> <span data-ttu-id="a9265-117">プロバイダーが **followPerson** をtrue に設定しているが **、ISocialSession2** インターフェイスを実装していない場合、または **FollowPersonEx** が OSC_E_NOTIMPL エラーを返す場合、OSC は **ISocialSession::FollowPerson** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a9265-117">If the provider has set **followPerson** as **true** but does not implement the **ISocialSession2** interface, or **FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC calls **ISocialSession::FollowPerson**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a9265-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9265-118">See also</span></span>

- [<span data-ttu-id="a9265-119">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a9265-119">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

