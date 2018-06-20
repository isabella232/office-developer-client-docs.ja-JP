---
title: ISocialSessionLoggedOnUserName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c0e7b788-3198-499c-ae21-b2032f929ed9
description: ログオン時に使用されるユーザー名を表す文字列を返します。
ms.openlocfilehash: 02485ad2a510a81c64406ea6ec9a0f85c0e4d2f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804487"
---
# <a name="isocialsessionloggedonusername"></a><span data-ttu-id="8f8f2-103">ISocialSession::LoggedOnUserName</span><span class="sxs-lookup"><span data-stu-id="8f8f2-103">ISocialSession::LoggedOnUserName</span></span>

<span data-ttu-id="8f8f2-104">ログオン時に使用されるユーザー名を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="8f8f2-104">Returns a string that represents the user name that is used when logging on.</span></span>
  
```cpp
[propget] HRESULT _stdcall LoggedOnUserName([out, retval] BSTR* result);
```

## <a name="property-value"></a><span data-ttu-id="8f8f2-105">プロパティ値</span><span class="sxs-lookup"><span data-stu-id="8f8f2-105">Property value</span></span>

<span data-ttu-id="8f8f2-106">ログオン ユーザーのユーザー名を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="8f8f2-106">A string that represents the user name of the logged-on user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8f8f2-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="8f8f2-107">See also</span></span>

- [<span data-ttu-id="8f8f2-108">ISocialSession::LoggedOnUserID</span><span class="sxs-lookup"><span data-stu-id="8f8f2-108">ISocialSession::LoggedOnUserID</span></span>](isocialsession-loggedonuserid.md)  
- [<span data-ttu-id="8f8f2-109">ISocialSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8f8f2-109">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

