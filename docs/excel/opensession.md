---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e4df0c5772f28ab4ab8d84eaddfe4409a88061b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421838"
---
# <a name="opensession"></a><span data-ttu-id="5fbb7-103">OpenSession</span><span class="sxs-lookup"><span data-stu-id="5fbb7-103">OpenSession</span></span>

<span data-ttu-id="5fbb7-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5fbb7-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5fbb7-105">ユーザー定義関数を実行できるセッションを作成します。</span><span class="sxs-lookup"><span data-stu-id="5fbb7-105">Creates a session in which user-defined functions can be executed.</span></span>
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a><span data-ttu-id="5fbb7-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5fbb7-106">Parameters</span></span>

<span data-ttu-id="5fbb7-107">_Params_</span><span class="sxs-lookup"><span data-stu-id="5fbb7-107">_Params_</span></span>
  
> <span data-ttu-id="5fbb7-p101">セッションのパラメーターの、セミコロンで区切られた UNICODE 文字列へのポインター。Excel では、この引数は使用しません。</span><span class="sxs-lookup"><span data-stu-id="5fbb7-p101">A pointer to semicolon-delimited UNICODE string of parameters for the session. Excel does not use this argument.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5fbb7-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="5fbb7-110">Return value</span></span>

<span data-ttu-id="5fbb7-111">セッションが正常に作成された場合は、このクラスター コネクタに対する他の呼び出しで使用するセッション ID。それ以外の場合は **xlHpcRetCallFailed**。</span><span class="sxs-lookup"><span data-stu-id="5fbb7-111">A session ID to use in other calls to the cluster connector, if the session was successfully created; otherwise **xlHpcRetCallFailed**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5fbb7-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="5fbb7-112">See also</span></span>

- [<span data-ttu-id="5fbb7-113">Excel クラスター コネクタ関数</span><span class="sxs-lookup"><span data-stu-id="5fbb7-113">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

