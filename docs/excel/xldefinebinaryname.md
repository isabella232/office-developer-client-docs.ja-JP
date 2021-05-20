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
ms.openlocfilehash: 3c7fc4f6b6fc7179c1ca84043895273b2781f8b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430253"
---
# <a name="xldefinebinaryname"></a><span data-ttu-id="4b97c-104">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="4b97c-104">xlDefineBinaryName</span></span>

 <span data-ttu-id="4b97c-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4b97c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4b97c-p101">Used to allocate persistent storage for an **xltypeBigData** **XLOPER**/ **XLOPER12**. Data with a defined binary name is saved with the workbook, and can be accessed by name at any time. For more information, see "Binary Name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="4b97c-p101">Used to allocate persistent storage for an **xltypeBigData** **XLOPER**/ **XLOPER12**. Data with a defined binary name is saved with the workbook, and can be accessed by name at any time. For more information, see "Binary Name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a><span data-ttu-id="4b97c-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4b97c-109">Parameters</span></span>

 <span data-ttu-id="4b97c-110">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="4b97c-110">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="4b97c-p102">データの名前を指定する文字列。文字列は、定義された名前と同じ命名の制限に従います。</span><span class="sxs-lookup"><span data-stu-id="4b97c-p102">A string specifying the name of the data. The string is subject to the same naming restrictions as defined names.</span></span>
  
 <span data-ttu-id="4b97c-113">_pxData_ (**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="4b97c-113">_pxData_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="4b97c-p103">格納するデータを指定する Bigdata 構造体。この関数を呼び出す際は、**Bigdata** 構造体の **lpbData** メンバーで、名前を定義するデータをポイントする必要があります。また、**cbData** メンバーには、データの長さ (バイト単位) を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b97c-p103">Bigdata structure specifying the data to be stored. When you call this function, the **lpbData** member of the **bigdata** structure should point to the data for which the name is being defined, and the **cbData** member should contain the length of the data in bytes.</span></span> 
  
<span data-ttu-id="4b97c-116">_pxData_ 引数が指定されていない場合 (**xltypeMissing**)、_pxName_ により指定された名前付きの割り当てが削除されます。</span><span class="sxs-lookup"><span data-stu-id="4b97c-116">If the  _pxData_ argument is not specified (**xltypeMissing**), the named allocation specified by  _pxName_ is deleted.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4b97c-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="4b97c-117">See also</span></span>



[<span data-ttu-id="4b97c-118">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="4b97c-118">xlGetBinaryName</span></span>](xlgetbinaryname.md)


[<span data-ttu-id="4b97c-119">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="4b97c-119">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="4b97c-120">Excel XLL 開発での既知の問題</span><span class="sxs-lookup"><span data-stu-id="4b97c-120">Known Issues in Excel XLL Development</span></span>](known-issues-in-excel-xll-development.md)

