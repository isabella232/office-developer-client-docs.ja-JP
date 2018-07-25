---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 782843f11643e203488b313181d224443a1d36c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798938"
---
# <a name="opensession"></a><span data-ttu-id="58c7b-103">OpenSession</span><span class="sxs-lookup"><span data-stu-id="58c7b-103">OpenSession</span></span>

<span data-ttu-id="58c7b-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="58c7b-104">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="58c7b-105">ユーザー定義関数を実行できるセッションを作成します。</span><span class="sxs-lookup"><span data-stu-id="58c7b-105">Creates a session in which user-defined functions can be executed.</span></span>
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a><span data-ttu-id="58c7b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="58c7b-106">Parameters</span></span>

<span data-ttu-id="58c7b-107">_Params_</span><span class="sxs-lookup"><span data-stu-id="58c7b-107">_Params_</span></span>
  
> <span data-ttu-id="58c7b-p101">セッションのパラメーターの、セミコロンで区切られた UNICODE 文字列へのポインター。Excel では、この引数は使用しません。</span><span class="sxs-lookup"><span data-stu-id="58c7b-p101">A pointer to semicolon-delimited UNICODE string of parameters for the session. Excel does not use this argument.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="58c7b-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="58c7b-110">Return value</span></span>

<span data-ttu-id="58c7b-111">セッションが正常に作成された場合は、このクラスター コネクタに対する他の呼び出しで使用するセッション ID。それ以外の場合は **xlHpcRetCallFailed**。</span><span class="sxs-lookup"><span data-stu-id="58c7b-111">A session ID to use in other calls to the cluster connector, if the session was successfully created; otherwise **xlHpcRetCallFailed**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="58c7b-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="58c7b-112">See also</span></span>

- [<span data-ttu-id="58c7b-113">Excel クラスター コネクタ関数</span><span class="sxs-lookup"><span data-stu-id="58c7b-113">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

