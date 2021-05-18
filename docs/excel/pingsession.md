---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0fa5fe57e537a7b8c7d880b934809a6f68ce27a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408363"
---
# <a name="pingsession"></a><span data-ttu-id="511ba-103">PingSession</span><span class="sxs-lookup"><span data-stu-id="511ba-103">PingSession</span></span>

<span data-ttu-id="511ba-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="511ba-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="511ba-p101">セッションが有効かどうかをチェックします。この関数は通常、以前返されたセッション ID が現在もアクティブで使用可能かどうかを Excel で判断する必要がある場合に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="511ba-p101">Checks whether a session is valid. This function is typically called when Excel needs to determine if a previously returned session ID is still active and can be used.</span></span>
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="511ba-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="511ba-107">Parameters</span></span>

<span data-ttu-id="511ba-108">_SessionID_</span><span class="sxs-lookup"><span data-stu-id="511ba-108">_SessionID_</span></span>
  
> <span data-ttu-id="511ba-p102">ping を実行するセッションの ID。この値は、前回 [OpenSession](opensession.md) を呼び出した際に返された ID と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="511ba-p102">The ID of the session to ping. This value must match an ID returned by a previous call to [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="511ba-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="511ba-111">Return value</span></span>

<span data-ttu-id="511ba-112">_SessionId_ 引数が有効な場合は **xlHpcRetSuccess** を返します。それ以外の場合は **xlHpcRetInvalidSessionId** を返します。</span><span class="sxs-lookup"><span data-stu-id="511ba-112">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; otherwise **xlHpcRetInvalidSessionId**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="511ba-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="511ba-113">See also</span></span>

- [<span data-ttu-id="511ba-114">OpenSession</span><span class="sxs-lookup"><span data-stu-id="511ba-114">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="511ba-115">Excel クラスター コネクタ関数</span><span class="sxs-lookup"><span data-stu-id="511ba-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

