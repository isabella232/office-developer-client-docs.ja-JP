---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Web 認証時にユーザーにブラウザー ベースのフォームを表示するために使用される URL を表す文字列を取得します。
ms.openlocfilehash: 343919f194b238fc519bb8f6d808b44a8ab6e7b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804359"
---
# <a name="isocialsessiongetlogonurl"></a><span data-ttu-id="a1e42-103">ISocialSession::GetLogonUrl</span><span class="sxs-lookup"><span data-stu-id="a1e42-103">ISocialSession::GetLogonUrl</span></span>

<span data-ttu-id="a1e42-104">Web 認証時にユーザーにブラウザー ベースのフォームを表示するために使用される URL を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="a1e42-104">Gets a string that represents a URL that is used for presenting a browser-based form to the user during web authentication.</span></span>
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a><span data-ttu-id="a1e42-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a1e42-105">Parameters</span></span>

<span data-ttu-id="a1e42-106">_url_</span><span class="sxs-lookup"><span data-stu-id="a1e42-106">_url_</span></span>
  
> <span data-ttu-id="a1e42-107">[out]Web 認証で使用するフォームの URL を含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="a1e42-107">[out] A string that contains a URL for the form used in web authentication.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a1e42-108">注釈</span><span class="sxs-lookup"><span data-stu-id="a1e42-108">Remarks</span></span>

<span data-ttu-id="a1e42-109">フォームは、ユーザーに提示された後は、 _connectIn_パラメーターに空の文字列で[ISocialSession::LogonWeb](isocialsession-logonweb.md)メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a1e42-109">After the form is presented to the user, the [ISocialSession::LogonWeb](isocialsession-logonweb.md) method is called with an empty string for the  _connectIn_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a1e42-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="a1e42-110">See also</span></span>

- [<span data-ttu-id="a1e42-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a1e42-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

