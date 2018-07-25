---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- xldefinebinaryname function [excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 14515cc262ea398a9f200c0de3a1f6b64c758b3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798962"
---
# <a name="xldefinebinaryname"></a><span data-ttu-id="d7548-104">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="d7548-104">xlDefineBinaryName</span></span>

 <span data-ttu-id="d7548-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d7548-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d7548-106">**xltypeBigData** **XLOPER**/ **XLOPER12** の永続ストレージを割り当てるために使用します。</span><span class="sxs-lookup"><span data-stu-id="d7548-106">Used to allocate persistent storage for an **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="d7548-107">定義されているバイナリ名が含まれるデータはブックに保存され、いつでも名前でアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d7548-107">Used to allocate persistent storage for an xltypeBigDataXLOPER/XLOPER12. Data with a defined binary name is saved with the workbook, and can be accessed by name at any time. For more information, see "Binary Name Scope Limitation" in Known Issues.</span></span> <span data-ttu-id="d7548-108">詳細については、「[Excel XLL 開発での既知の問題](known-issues-in-excel-xll-development.md)」の「バイナリ名のスコープ制限」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d7548-108">For more information, see "Binary Name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a><span data-ttu-id="d7548-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d7548-109">Parameters</span></span>

 <span data-ttu-id="d7548-110">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="d7548-110">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="d7548-p102">データの名前を指定する文字列。文字列は、定義された名前と同じ命名の制限に従います。</span><span class="sxs-lookup"><span data-stu-id="d7548-p102">A string specifying the name of the data. The string is subject to the same naming restrictions as defined names.</span></span>
  
 <span data-ttu-id="d7548-113">_pxData_ (**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="d7548-113">_pxData_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="d7548-p103">格納するデータを指定する Bigdata 構造体。この関数を呼び出す際は、**Bigdata** 構造体の **lpbData** メンバーで、名前を定義するデータをポイントする必要があります。また、**cbData** メンバーには、データの長さ (バイト単位) を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7548-p103">Bigdata structure specifying the data to be stored. When you call this function, the **lpbData** member of the **bigdata** structure should point to the data for which the name is being defined, and the **cbData** member should contain the length of the data in bytes.</span></span> 
  
<span data-ttu-id="d7548-116">_pxData_ 引数が指定されていない場合 (**xltypeMissing**)、_pxName_ により指定された名前付きの割り当てが削除されます。</span><span class="sxs-lookup"><span data-stu-id="d7548-116">If the _pxData_ argument is not specified (**xltypeMissing**), the named allocation specified by _pxName_ is deleted.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d7548-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="d7548-117">See also</span></span>



[<span data-ttu-id="d7548-118">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="d7548-118">xlGetBinaryName</span></span>](xlgetbinaryname.md)


[<span data-ttu-id="d7548-119">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="d7548-119">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="d7548-120">Excel XLL 開発での既知の問題</span><span class="sxs-lookup"><span data-stu-id="d7548-120">Known Issues in Excel XLL Development</span></span>](known-issues-in-excel-xll-development.md)

