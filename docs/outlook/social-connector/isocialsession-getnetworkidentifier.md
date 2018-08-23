---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: 特定のソーシャル ネットワークの接続のソーシャル ネットワークの一意の識別子を表す文字列を取得します。
ms.openlocfilehash: eb618ba8e8bb37278c1fdb09d984fba141a9d686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804486"
---
# <a name="isocialsessiongetnetworkidentifier"></a><span data-ttu-id="38729-103">ISocialSession::GetNetworkIdentifier</span><span class="sxs-lookup"><span data-stu-id="38729-103">ISocialSession::GetNetworkIdentifier</span></span>

<span data-ttu-id="38729-104">特定のソーシャル ネットワークの接続のソーシャル ネットワークの一意の識別子を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="38729-104">Gets a string that represents a unique social network identifier for a given social network connection.</span></span> 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a><span data-ttu-id="38729-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="38729-105">Parameters</span></span>

<span data-ttu-id="38729-106">_networkIdentifier_</span><span class="sxs-lookup"><span data-stu-id="38729-106">_networkIdentifier_</span></span>
  
> <span data-ttu-id="38729-107">[out]ソーシャル ネットワークの一意な識別子を含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="38729-107">[out] A string that contains a unique social network identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38729-108">注釈</span><span class="sxs-lookup"><span data-stu-id="38729-108">Remarks</span></span>

<span data-ttu-id="38729-109">ネットワークの一意の識別子は、Outlook ソーシャル コネクタ (OSC) プロバイダーのソーシャル ネットワークを識別する文字列です。</span><span class="sxs-lookup"><span data-stu-id="38729-109">A unique network identifier is a string that identifies the Outlook Social Connector (OSC) provider social network.</span></span> <span data-ttu-id="38729-110">このメソッドは E_NOTIMPL を返すこともします。</span><span class="sxs-lookup"><span data-stu-id="38729-110">This method can also return E_NOTIMPL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="38729-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="38729-111">See also</span></span>

- [<span data-ttu-id="38729-112">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="38729-112">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

