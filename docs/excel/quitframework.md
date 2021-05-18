---
title: QuitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- QuitFramework
keywords:
- quitframework function
localization_priority: Normal
ms.assetid: d17a3efe-c278-4ef1-b8f9-b958ae012361
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9408a7938927214802935e54ec8e53b1469e5016
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408573"
---
# <a name="quitframework"></a><span data-ttu-id="f49cb-104">QuitFramework</span><span class="sxs-lookup"><span data-stu-id="f49cb-104">QuitFramework</span></span>

 <span data-ttu-id="f49cb-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f49cb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f49cb-106">フレームワーク ライブラリを初期化しないフレームワーク ライブラリ関数。これは単に、既に割り当てられているメモリを解放して、一時 **XLOPER**/ **XLOPER12** のメモリ データ構造を再初期化します。</span><span class="sxs-lookup"><span data-stu-id="f49cb-106">Framework library function that uninitializes the Framework library, which simply re-initializes the temporary **XLOPER**/ **XLOPER12** memory data structures, freeing any memory that has already been allocated.</span></span> 
  
```cs
short WINAPI QuitFramework(void);
```

## <a name="parameters"></a><span data-ttu-id="f49cb-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f49cb-107">Parameters</span></span>

<span data-ttu-id="f49cb-108">この関数に引数はありません。</span><span class="sxs-lookup"><span data-stu-id="f49cb-108">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f49cb-109">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="f49cb-109">Property value/Return value</span></span>

<span data-ttu-id="f49cb-110">この関数は値を返しません。</span><span class="sxs-lookup"><span data-stu-id="f49cb-110">This function does not return a value.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f49cb-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="f49cb-111">See also</span></span>



[<span data-ttu-id="f49cb-112">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="f49cb-112">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

