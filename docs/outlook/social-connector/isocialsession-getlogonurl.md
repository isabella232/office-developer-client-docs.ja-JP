---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Web 認証中にブラウザー ベースのフォームをユーザーに表示するために使用される URL を表す文字列を取得します。
ms.openlocfilehash: 83867282922ea136b9673609cc2ba2f1a206f6ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427914"
---
# <a name="isocialsessiongetlogonurl"></a><span data-ttu-id="3e9b4-103">ISocialSession::GetLogonUrl</span><span class="sxs-lookup"><span data-stu-id="3e9b4-103">ISocialSession::GetLogonUrl</span></span>

<span data-ttu-id="3e9b4-104">Web 認証中にブラウザー ベースのフォームをユーザーに表示するために使用される URL を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="3e9b4-104">Gets a string that represents a URL that is used for presenting a browser-based form to the user during web authentication.</span></span>
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a><span data-ttu-id="3e9b4-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3e9b4-105">Parameters</span></span>

<span data-ttu-id="3e9b4-106">_url_</span><span class="sxs-lookup"><span data-stu-id="3e9b4-106">_url_</span></span>
  
> <span data-ttu-id="3e9b4-107">[out]Web 認証で使用されるフォームの URL を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="3e9b4-107">[out] A string that contains a URL for the form used in web authentication.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3e9b4-108">注釈</span><span class="sxs-lookup"><span data-stu-id="3e9b4-108">Remarks</span></span>

<span data-ttu-id="3e9b4-109">フォームがユーザーに提示された後 [、iSocialSession::LogonWeb](isocialsession-logonweb.md) メソッドは  _、connectIn_ パラメーターの空の文字列で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3e9b4-109">After the form is presented to the user, the [ISocialSession::LogonWeb](isocialsession-logonweb.md) method is called with an empty string for the  _connectIn_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3e9b4-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="3e9b4-110">See also</span></span>

- [<span data-ttu-id="3e9b4-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3e9b4-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

