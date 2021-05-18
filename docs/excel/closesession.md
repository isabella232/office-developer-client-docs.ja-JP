---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9186fb14c33d507b8c9ae709a67f1b43e6206d5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422538"
---
# <a name="closesession"></a><span data-ttu-id="30c93-103">CloseSession</span><span class="sxs-lookup"><span data-stu-id="30c93-103">CloseSession</span></span>

<span data-ttu-id="30c93-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="30c93-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="30c93-105">クラスターでセッションを終了します。</span><span class="sxs-lookup"><span data-stu-id="30c93-105">Ends a session with a cluster.</span></span>
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="30c93-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="30c93-106">Parameters</span></span>

<span data-ttu-id="30c93-107">_SessionId_</span><span class="sxs-lookup"><span data-stu-id="30c93-107">_SessionId_</span></span>
  
> <span data-ttu-id="30c93-p101">閉じるセッションの ID。この値は、[OpenSession](opensession.md) で返された値に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30c93-p101">The ID of the session to close. This value must match the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="30c93-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="30c93-110">Return value</span></span>

<span data-ttu-id="30c93-111">セッションが閉じられた場合は **xlHpcRetSuccess** が返されます。_SessionId_ 引数が無効な場合は **xlHpcRetInvalidSessionId**、その他のエラーが発生した場合は **xlHpcRetCallFailed** が返されます。</span><span class="sxs-lookup"><span data-stu-id="30c93-111">**xlHpcRetSuccess** if the session closed; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="30c93-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="30c93-112">See also</span></span>

- [<span data-ttu-id="30c93-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="30c93-113">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="30c93-114">Excel クラスター コネクタ関数</span><span class="sxs-lookup"><span data-stu-id="30c93-114">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

