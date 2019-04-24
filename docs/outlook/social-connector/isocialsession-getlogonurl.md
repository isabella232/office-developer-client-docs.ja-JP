---
title: i、alsessiongetlogonurl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: web 認証中にブラウザーベースのフォームをユーザーに提示するために使用される URL を表す文字列を取得します。
ms.openlocfilehash: 83867282922ea136b9673609cc2ba2f1a206f6ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285379"
---
# <a name="isocialsessiongetlogonurl"></a><span data-ttu-id="9a80a-103">ISocialSession::GetLogonUrl</span><span class="sxs-lookup"><span data-stu-id="9a80a-103">ISocialSession::GetLogonUrl</span></span>

<span data-ttu-id="9a80a-104">web 認証中にブラウザーベースのフォームをユーザーに提示するために使用される URL を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="9a80a-104">Gets a string that represents a URL that is used for presenting a browser-based form to the user during web authentication.</span></span>
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a><span data-ttu-id="9a80a-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9a80a-105">Parameters</span></span>

<span data-ttu-id="9a80a-106">_url_</span><span class="sxs-lookup"><span data-stu-id="9a80a-106">_url_</span></span>
  
> <span data-ttu-id="9a80a-107">読み上げweb 認証で使用するフォームの URL を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="9a80a-107">[out] A string that contains a URL for the form used in web authentication.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a80a-108">解説</span><span class="sxs-lookup"><span data-stu-id="9a80a-108">Remarks</span></span>

<span data-ttu-id="9a80a-109">フォームがユーザーに表示された後、i渡された[alsession:: logonweb](isocialsession-logonweb.md)メソッドが、ユーザーに空の__ 文字列を指定して呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9a80a-109">After the form is presented to the user, the [ISocialSession::LogonWeb](isocialsession-logonweb.md) method is called with an empty string for the  _connectIn_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9a80a-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="9a80a-110">See also</span></span>

- [<span data-ttu-id="9a80a-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a80a-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

