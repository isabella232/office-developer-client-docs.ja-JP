---
title: ISocialSessionLoggedOnUserID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54377ab4-8c69-4d7a-b9b7-278241823c8d
description: 現在ログオンしているユーザーのソーシャル ネットワーク ユーザー ID を表す文字列を返します。
ms.openlocfilehash: edb61569829f7690c2284a083d2cbd5cfe2d32a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413571"
---
# <a name="isocialsessionloggedonuserid"></a><span data-ttu-id="09023-103">ISocialSession::LoggedOnUserID</span><span class="sxs-lookup"><span data-stu-id="09023-103">ISocialSession::LoggedOnUserID</span></span>

<span data-ttu-id="09023-104">現在ログオンしているユーザーのソーシャル ネットワーク ユーザー ID を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="09023-104">Returns a string that represents the social network user ID of the user who is currently logged on.</span></span> 
  
```cpp
[propget] HRESULT _stdcall LoggedOnUserID([out, retval] BSTR* result);
```

## <a name="property-value"></a><span data-ttu-id="09023-105">プロパティ値</span><span class="sxs-lookup"><span data-stu-id="09023-105">Property value</span></span>

<span data-ttu-id="09023-106">ログオンしているユーザーのソーシャル ネットワーク ユーザー ID を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="09023-106">A string that contains the social network user ID of the logged-on user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="09023-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="09023-107">See also</span></span>

- [<span data-ttu-id="09023-108">ISocialSession::LoggedOnUserName</span><span class="sxs-lookup"><span data-stu-id="09023-108">ISocialSession::LoggedOnUserName</span></span>](isocialsession-loggedonusername.md)  
- [<span data-ttu-id="09023-109">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="09023-109">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

