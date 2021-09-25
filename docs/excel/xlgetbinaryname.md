---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- xlgetbinaryname function [excel 2007]
ms.localizationpriority: medium
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 84581705359442ce9366d1602920195c63c36375
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596793"
---
# <a name="xlgetbinaryname"></a>xlGetBinaryName

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Used to return a handle for data saved by the [xlDefineBinaryName function](xldefinebinaryname.md). Data with a defined binary name is saved with the workbook and can be accessed by name at any time. For more information, see "Binary name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a>パラメーター

_pxRes_ (**xltypeBigData** または **xltypeErr**)
  
取得されたデータまたはエラーを指定する Bigdata 構造体は、取得できなかったデータまたは定義されていない名前になります。関数が戻った時点で、**XLOPER**/ **XLOPER12** の **hdata** メンバーに名前付きデータのハンドルが格納されています。_pxRes_ が不要になったら、**xlFree** の呼び出しでこれを解放する必要があります。 
  
_pxName_ (**xltypeStr**)
  
データの名前を指定する文字列。
  
## <a name="remarks"></a>注釈

Microsoft Excel は、**hdata** で返されたメモリ ハンドルを所有します。Windows では、このハンドルはグローバル メモリ ハンドルです (**GlobalAlloc** 関数によって割り当てられます)。 
  
## <a name="see-also"></a>関連項目

- [xlDefineBinaryName](xldefinebinaryname.md)
- [DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

