---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1d55f22de88b274d0403f81717d0fddefbea0219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798761"
---
# <a name="calludf"></a><span data-ttu-id="ebdbd-103">CallUDF</span><span class="sxs-lookup"><span data-stu-id="ebdbd-103">CallUDF</span></span>

<span data-ttu-id="ebdbd-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ebdbd-104">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ebdbd-105">高パフォーマンスのコンピューティング環境でユーザー定義関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ebdbd-105">Calls a user-defined function in a high-performance computing environment.</span></span>
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a><span data-ttu-id="ebdbd-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ebdbd-106">Parameters</span></span>

<span data-ttu-id="ebdbd-107">_SessionId_</span><span class="sxs-lookup"><span data-stu-id="ebdbd-107">_SessionId_</span></span>
  
> <span data-ttu-id="ebdbd-108">呼び出しを行うセッションの ID。</span><span class="sxs-lookup"><span data-stu-id="ebdbd-108">The ID of the session in which to make the call.</span></span>
    
<span data-ttu-id="ebdbd-109">_XLLName_</span><span class="sxs-lookup"><span data-stu-id="ebdbd-109">_XLLName_</span></span>
  
> <span data-ttu-id="ebdbd-110">ユーザー定義関数が含まれる XLL の名前。</span><span class="sxs-lookup"><span data-stu-id="ebdbd-110">The name of the XLL that contains the user-defined function.</span></span>
    
<span data-ttu-id="ebdbd-111">_UDFName_</span><span class="sxs-lookup"><span data-stu-id="ebdbd-111">_UDFName_</span></span>
  
> <span data-ttu-id="ebdbd-112">ユーザー定義関数の名前。</span><span class="sxs-lookup"><span data-stu-id="ebdbd-112">The name of the user-defined function.</span></span>
    
<span data-ttu-id="ebdbd-113">_CallBackAddr_</span><span class="sxs-lookup"><span data-stu-id="ebdbd-113">_CallBackAddr_</span></span>
  
> <span data-ttu-id="ebdbd-114">ユーザー定義関数が終了するときにコネクタが呼び出す必要がある関数。</span><span class="sxs-lookup"><span data-stu-id="ebdbd-114">The function that the connector should call when the user-defined function is finished.</span></span>
    
<span data-ttu-id="ebdbd-115">_pxAsyncHandle_</span><span class="sxs-lookup"><span data-stu-id="ebdbd-115">_pxAsyncHandle_</span></span>
  
> <span data-ttu-id="ebdbd-p101">Excel とコネクタが、保留中のユーザー定義関数の呼び出しを追跡するために使用する非同期ハンドル。コネクタはこれを使用して、呼び出しが完了した時点で、_CallBackAddr_ 引数で渡された関数ポインターを使用して Excel へのコールバックを行います。</span><span class="sxs-lookup"><span data-stu-id="ebdbd-p101">The asynchronous handle used by Excel and the connector to track the pending user-defined function call. The connector uses it later when the call is finished, when it calls back into Excel using the function pointer passed in the  _CallBackAddr_ argument.</span></span> 
    
<span data-ttu-id="ebdbd-118">_ArgCount_</span><span class="sxs-lookup"><span data-stu-id="ebdbd-118">_ArgCount_</span></span>
  
> <span data-ttu-id="ebdbd-p102">ユーザー定義関数に渡される引数の数。最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="ebdbd-p102">The number of arguments to pass to the user-defined function. The maximum value allowed is 255.</span></span>
    
<span data-ttu-id="ebdbd-121">_Parameter1_</span><span class="sxs-lookup"><span data-stu-id="ebdbd-121">_Parameter1_</span></span>
  
> <span data-ttu-id="ebdbd-p103">ユーザー定義関数に渡す値。_ArgCount_ で指定されたパラメーターごとに、この引数を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="ebdbd-p103">A value to pass to the user-defined function. Repeat this argument for each parameter indicated by  _ArgCount_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ebdbd-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="ebdbd-124">Return value</span></span>

<span data-ttu-id="ebdbd-125">UDF 呼び出しが正常に開始された場合は **xlHpcRetSuccess** が返されます。_SessionId_ 引数が無効な場合は **xlHpcRetInvalidSessionId**、タイムアウトなどのその他のエラーが発生した場合は **xlHpcRetCallFailed** が返されます。呼び出しがエラー コード (**xlHpcRetSuccess** 以外のすべてのコード) を返すと、Excel は UDF 呼び出しが失敗したとみなし、_pxAsyncHandle_ を無効化します。この場合、Excel はコールバックが行われることを期待しません。</span><span class="sxs-lookup"><span data-stu-id="ebdbd-125">**xlHpcRetSuccess** if the UDF call is successfully initiated; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures, including time-out. If the call returns any error code (anything except **xlHpcRetSuccess**), then Excel considers the UDF call to have failed, invalidates the  _pxAsyncHandle_, and does not expect a callback to occur.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ebdbd-126">注釈</span><span class="sxs-lookup"><span data-stu-id="ebdbd-126">Remarks</span></span>

<span data-ttu-id="ebdbd-127">この関数は非同期で実行されます。</span><span class="sxs-lookup"><span data-stu-id="ebdbd-127">This function executes asynchronously.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ebdbd-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="ebdbd-128">See also</span></span>

- [<span data-ttu-id="ebdbd-129">Excel クラスター コネクタ関数</span><span class="sxs-lookup"><span data-stu-id="ebdbd-129">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

