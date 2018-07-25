---
title: xlRunningOnCluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- xlrunningoncluster
localization_priority: Normal
ms.assetid: 7662f255-4184-4af0-97f5-9a89347a201a
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f42ccbeb94e1fc6b6cf880f1b32ee1bfeb24997e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799009"
---
# <a name="xlrunningoncluster"></a><span data-ttu-id="d7148-104">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="d7148-104">xlRunningOnCluster</span></span>

<span data-ttu-id="d7148-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d7148-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d7148-106">ユーザー定義関数がクラスターで実行されているかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="d7148-106">Returns a value that indicates whether the user-defined function is running on a cluster.</span></span> 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="d7148-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d7148-107">Parameters</span></span>

<span data-ttu-id="d7148-108">この関数には引数はありません。</span><span class="sxs-lookup"><span data-stu-id="d7148-108">This function has no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="d7148-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="d7148-109">Return value</span></span>

<span data-ttu-id="d7148-p101">この関数が Excel プロセスで実行される場合、**xlTypeInt** 型の **XLOPER12** で 0 が返されます。関数がクラスター上で実行される場合、戻り値の型と値は、クラスター コネクタ プロバイダーによって決まります。</span><span class="sxs-lookup"><span data-stu-id="d7148-p101">If the function is running in an Excel process, returns 0 in an **XLOPER12** of type **xlTypeInt**. If the function is running on a cluster, the return type and value is determined by the cluster connector provider.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="d7148-112">要件</span><span class="sxs-lookup"><span data-stu-id="d7148-112">Requirements</span></span>

<span data-ttu-id="d7148-113">この関数は、Xlcall.h ヘッダー ファイルで定義されます。</span><span class="sxs-lookup"><span data-stu-id="d7148-113">This function is defined in the Xlcall.h header file.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d7148-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="d7148-114">See also</span></span>

- [<span data-ttu-id="d7148-115">クラスター セーフ関数</span><span class="sxs-lookup"><span data-stu-id="d7148-115">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
- [<span data-ttu-id="d7148-116">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="d7148-116">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

