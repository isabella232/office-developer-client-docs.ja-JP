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
ms.localizationpriority: medium
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 17a28b5fac2e2d92beb19def39174a728df1b188
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611211"
---
# <a name="xldefinebinaryname"></a>xlDefineBinaryName

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Used to allocate persistent storage for an **xltypeBigData** **XLOPER**/ **XLOPER12**. Data with a defined binary name is saved with the workbook, and can be accessed by name at any time. For more information, see "Binary Name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a>パラメーター

 _pxName_ (**xltypeStr**)
  
データの名前を指定する文字列。文字列は、定義された名前と同じ命名の制限に従います。
  
 _pxData_ (**xltypeBigData**)
  
格納するデータを指定する Bigdata 構造体。この関数を呼び出す際は、**Bigdata** 構造体の **lpbData** メンバーで、名前を定義するデータをポイントする必要があります。また、**cbData** メンバーには、データの長さ (バイト単位) を含める必要があります。 
  
_pxData_ 引数が指定されていない場合 (**xltypeMissing**)、_pxName_ により指定された名前付きの割り当てが削除されます。 
  
## <a name="see-also"></a>関連項目



[xlGetBinaryName](xlgetbinaryname.md)


[DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Excel XLL 開発での既知の問題](known-issues-in-excel-xll-development.md)

