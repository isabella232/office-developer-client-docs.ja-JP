---
title: ISocialSessionLoggedOnUserID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54377ab4-8c69-4d7a-b9b7-278241823c8d
description: 現在ログオンしているユーザーのソーシャル ネットワークのユーザー ID を表す文字列を返します。
ms.openlocfilehash: dcc81d7acf8a839e7fe3249cc0eb06f96c113b56
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804365"
---
# <a name="isocialsessionloggedonuserid"></a><span data-ttu-id="b177c-103">ISocialSession::LoggedOnUserID</span><span class="sxs-lookup"><span data-stu-id="b177c-103">ISocialSession::LoggedOnUserID</span></span>

<span data-ttu-id="b177c-104">現在ログオンしているユーザーのソーシャル ネットワークのユーザー ID を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="b177c-104">Returns a string that represents the social network user ID of the user who is currently logged on.</span></span> 
  
```cpp
[propget] HRESULT _stdcall LoggedOnUserID([out, retval] BSTR* result);
```

## <a name="property-value"></a><span data-ttu-id="b177c-105">プロパティ値</span><span class="sxs-lookup"><span data-stu-id="b177c-105">Property value</span></span>

<span data-ttu-id="b177c-106">ログオンしたユーザーのソーシャル ネットワークのユーザー ID を含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="b177c-106">A string that contains the social network user ID of the logged-on user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b177c-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="b177c-107">See also</span></span>

- [<span data-ttu-id="b177c-108">ISocialSession::LoggedOnUserName</span><span class="sxs-lookup"><span data-stu-id="b177c-108">ISocialSession::LoggedOnUserName</span></span>](isocialsession-loggedonusername.md)  
- [<span data-ttu-id="b177c-109">ISocialSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b177c-109">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

