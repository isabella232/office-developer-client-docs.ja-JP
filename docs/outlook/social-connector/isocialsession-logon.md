---
title: i、alsessionlogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b3c9a23-6378-4054-ad1c-193fc15c473c
description: 指定したユーザー名とパスワードを使用して、ソーシャルネットワークサイトにログオンします。
ms.openlocfilehash: 7915097e456d6fafa713901f8074e6531bfaa001
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361041"
---
# <a name="isocialsessionlogon"></a><span data-ttu-id="68394-103">ISocialSession::Logon</span><span class="sxs-lookup"><span data-stu-id="68394-103">ISocialSession::Logon</span></span>

<span data-ttu-id="68394-104">指定したユーザー名とパスワードを使用して、ソーシャルネットワークサイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="68394-104">Logs on to the social network site by using the specified user name and password.</span></span>
  
```cpp
HRESULT _stdcall Logon([in] BSTR username, [in] BSTR password);
```

## <a name="parameters"></a><span data-ttu-id="68394-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68394-105">Parameters</span></span>

<span data-ttu-id="68394-106">_<_</span><span class="sxs-lookup"><span data-stu-id="68394-106">_username_</span></span>
  
> <span data-ttu-id="68394-107">順番ログオンするユーザー名を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="68394-107">[in] A string that contains the user name to log on.</span></span>
    
<span data-ttu-id="68394-108">_password_</span><span class="sxs-lookup"><span data-stu-id="68394-108">_password_</span></span>
  
> <span data-ttu-id="68394-109">順番ログオンするパスワードを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="68394-109">[in] A string that contains the password to log on.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68394-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="68394-110">See also</span></span>

- [<span data-ttu-id="68394-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="68394-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

