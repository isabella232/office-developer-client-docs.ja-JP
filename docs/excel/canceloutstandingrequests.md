---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 882458ab096cbced8e0635dab65fe0b1d680388f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414719"
---
# <a name="canceloutstandingrequests"></a><span data-ttu-id="08d91-103">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="08d91-103">CancelOutstandingRequests</span></span>

<span data-ttu-id="08d91-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="08d91-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="08d91-105">Excel Calculation が取り消されたことをクラスター コネクタに通知します。そのため、そのセッションにおいて保留中の関数のすべての呼び出しも取り消される可能性があります (その Excel では、結果を伴うコールバックは必要ありません)。</span><span class="sxs-lookup"><span data-stu-id="08d91-105">Informs the cluster connector that an Excel calculation has been canceled, and therefore all pending function calls within that session may be cancelled as well (and that Excel does not expect callbacks with their results).</span></span>
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="08d91-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="08d91-106">Parameters</span></span>

<span data-ttu-id="08d91-107">_SessionID_</span><span class="sxs-lookup"><span data-stu-id="08d91-107">_SessionID_</span></span>
  
> <span data-ttu-id="08d91-p101">取り消された計算で使用されているセッションの ID。この値は、[OpenSession](opensession.md) によって返された値と一致します。</span><span class="sxs-lookup"><span data-stu-id="08d91-p101">The ID of the session used by the canceled calculation. This value matches the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="08d91-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="08d91-110">Return value</span></span>

<span data-ttu-id="08d91-111">_SessionId_ 引数が有効な場合は **xlHpcRetSuccess** が返されます。_SessionId_ 引数が無効な場合は **xlHpcRetInvalidSessionId**、その他のエラーが発生した場合は **xlHpcRetCallFailed** が返されます。</span><span class="sxs-lookup"><span data-stu-id="08d91-111">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="08d91-112">注釈</span><span class="sxs-lookup"><span data-stu-id="08d91-112">Remarks</span></span>

<span data-ttu-id="08d91-113">この呼び出し後に受け取る結果はすべて Excel によって破棄されるため、パフォーマンスを向上させるには、実装側でセッションのすべてのプロセスを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08d91-113">Implementers should stop all processes for the session for improved performance, as any results received after this call will be discarded by Excel.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="08d91-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="08d91-114">See also</span></span>

- [<span data-ttu-id="08d91-115">Excel クラスター コネクタ関数</span><span class="sxs-lookup"><span data-stu-id="08d91-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

