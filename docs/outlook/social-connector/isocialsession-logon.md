---
title: ISocialSessionLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b3c9a23-6378-4054-ad1c-193fc15c473c
description: 指定されたユーザー名とパスワードを使用して、ソーシャル ネットワーク サイトにログオンします。
ms.openlocfilehash: d7a79767f3726f9748ea48839f1e190af2e9ec74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804367"
---
# <a name="isocialsessionlogon"></a><span data-ttu-id="715ce-103">ISocialSession::Logon</span><span class="sxs-lookup"><span data-stu-id="715ce-103">ISocialSession::Logon</span></span>

<span data-ttu-id="715ce-104">指定されたユーザー名とパスワードを使用して、ソーシャル ネットワーク サイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="715ce-104">Logs on to the social network site by using the specified user name and password.</span></span>
  
```cpp
HRESULT _stdcall Logon([in] BSTR username, [in] BSTR password);
```

## <a name="parameters"></a><span data-ttu-id="715ce-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="715ce-105">Parameters</span></span>

<span data-ttu-id="715ce-106">_ユーザー名_</span><span class="sxs-lookup"><span data-stu-id="715ce-106">_username_</span></span>
  
> <span data-ttu-id="715ce-107">[in]ログオンするユーザー名を含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="715ce-107">[in] A string that contains the user name to log on.</span></span>
    
<span data-ttu-id="715ce-108">_password_</span><span class="sxs-lookup"><span data-stu-id="715ce-108">_password_</span></span>
  
> <span data-ttu-id="715ce-109">[in]ログオン時にパスワードを含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="715ce-109">[in] A string that contains the password to log on.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="715ce-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="715ce-110">See also</span></span>

- [<span data-ttu-id="715ce-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="715ce-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

