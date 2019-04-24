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
ms.openlocfilehash: 6f0d2c68b1af9e7c96f2cd86dc798518e432c7cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285307"
---
# <a name="isocialsessionloggedonusername"></a><span data-ttu-id="7af90-103">ISocialSession::LoggedOnUserName</span><span class="sxs-lookup"><span data-stu-id="7af90-103">ISocialSession::LoggedOnUserName</span></span>

<span data-ttu-id="7af90-104">ログオン時に使用されるユーザー名を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="7af90-104">Returns a string that represents the user name that is used when logging on.</span></span>
  
```cpp
[propget] HRESULT _stdcall LoggedOnUserName([out, retval] BSTR* result);
```

## <a name="property-value"></a><span data-ttu-id="7af90-105">プロパティ値</span><span class="sxs-lookup"><span data-stu-id="7af90-105">Property value</span></span>

<span data-ttu-id="7af90-106">ログオンしているユーザーのユーザー名を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="7af90-106">A string that represents the user name of the logged-on user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7af90-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="7af90-107">See also</span></span>

- [<span data-ttu-id="7af90-108">ISocialSession::LoggedOnUserID</span><span class="sxs-lookup"><span data-stu-id="7af90-108">ISocialSession::LoggedOnUserID</span></span>](isocialsession-loggedonuserid.md)  
- [<span data-ttu-id="7af90-109">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7af90-109">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

