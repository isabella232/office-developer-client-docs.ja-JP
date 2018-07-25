---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- initframework function [excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2d7e3286d794d6f21da9ef83ca44d18ec242c063
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798879"
---
# <a name="initframework"></a><span data-ttu-id="9a164-104">InitFramework</span><span class="sxs-lookup"><span data-stu-id="9a164-104">InitFramework</span></span>

 <span data-ttu-id="9a164-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9a164-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9a164-106">フレームワーク ライブラリを初期化するフレームワーク ライブラリ関数。これは単に、既に割り当てられているメモリを解放して、一時 **XLOPER**/ **XLOPER12** のメモリ データ構造を初期化します。</span><span class="sxs-lookup"><span data-stu-id="9a164-106">Framework library function that initializes the Framework library, which simply initializes the temporary **XLOPER**/ **XLOPER12** memory data structures, freeing any memory that has already been allocated.</span></span> 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a><span data-ttu-id="9a164-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9a164-107">Parameters</span></span>

<span data-ttu-id="9a164-108">この関数に引数はありません。</span><span class="sxs-lookup"><span data-stu-id="9a164-108">This function takes no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="9a164-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="9a164-109">Return value</span></span>

<span data-ttu-id="9a164-110">この関数は値を返しません。</span><span class="sxs-lookup"><span data-stu-id="9a164-110">This function does not return a value.</span></span>
  
## <a name="example"></a><span data-ttu-id="9a164-111">例</span><span class="sxs-lookup"><span data-stu-id="9a164-111">Example</span></span>

<span data-ttu-id="9a164-112">この例では **InitFramework** 関数を使用して、すべての一時メモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="9a164-112">This example uses the **InitFramework** function to free all temporary memory.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="9a164-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="9a164-113">See also</span></span>



[<span data-ttu-id="9a164-114">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="9a164-114">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

