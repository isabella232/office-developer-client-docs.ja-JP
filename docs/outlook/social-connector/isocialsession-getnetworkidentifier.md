---
title: i識別 alsessiongetnetworkidentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: 特定のソーシャルネットワーク接続の一意のソーシャルネットワーク識別子を表す文字列を取得します。
ms.openlocfilehash: 3051abd6dcccec878e8c53332980731772d543eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285338"
---
# <a name="isocialsessiongetnetworkidentifier"></a><span data-ttu-id="5dbb7-103">ISocialSession::GetNetworkIdentifier</span><span class="sxs-lookup"><span data-stu-id="5dbb7-103">ISocialSession::GetNetworkIdentifier</span></span>

<span data-ttu-id="5dbb7-104">特定のソーシャルネットワーク接続の一意のソーシャルネットワーク識別子を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="5dbb7-104">Gets a string that represents a unique social network identifier for a given social network connection.</span></span> 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a><span data-ttu-id="5dbb7-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5dbb7-105">Parameters</span></span>

<span data-ttu-id="5dbb7-106">_networkidentifier_</span><span class="sxs-lookup"><span data-stu-id="5dbb7-106">_networkIdentifier_</span></span>
  
> <span data-ttu-id="5dbb7-107">読み上げ一意のソーシャルネットワーク識別子を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="5dbb7-107">[out] A string that contains a unique social network identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5dbb7-108">解説</span><span class="sxs-lookup"><span data-stu-id="5dbb7-108">Remarks</span></span>

<span data-ttu-id="5dbb7-109">一意のネットワーク識別子は、Outlook social Connector (.osc) プロバイダーのソーシャルネットワークを識別する文字列です。</span><span class="sxs-lookup"><span data-stu-id="5dbb7-109">A unique network identifier is a string that identifies the Outlook Social Connector (OSC) provider social network.</span></span> <span data-ttu-id="5dbb7-110">このメソッドは、E_NOTIMPL を返すこともできます。</span><span class="sxs-lookup"><span data-stu-id="5dbb7-110">This method can also return E_NOTIMPL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5dbb7-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="5dbb7-111">See also</span></span>

- [<span data-ttu-id="5dbb7-112">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5dbb7-112">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

