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
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d2332967e798b43a350c0733cd7398e2a921add6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798978"
---
# <a name="xlgetbinaryname"></a>xlGetBinaryName

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
[xlDefineBinaryName 関数](xldefinebinaryname.md)によって保存されたデータのハンドルを返すのに使用されます。 定義されているバイナリ名が含まれるデータはブックに保存され、いつでも名前でアクセスできます。 詳細については、「[Excel XLL 開発での既知の問題](known-issues-in-excel-xll-development.md)」の「バイナリ名のスコープ制限」を参照してください。
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a>パラメーター

_pxRes _ (**xltypeBigData** または **xltypeErr**)
  
取得されたデータまたはエラーを指定する Bigdata 構造体は、取得できなかったデータまたは定義されていない名前になります。関数が戻った時点で、**XLOPER**/ **XLOPER12** の **hdata** メンバーに名前付きデータのハンドルが格納されています。_pxRes_ が不要になったら、**xlFree** の呼び出しでこれを解放する必要があります。 
  
_pxName_ (**xltypeStr**)
  
データの名前を指定する文字列。
  
## <a name="remarks"></a>注釈

Microsoft Excel は、**hdata** で返されたメモリ ハンドルを所有します。Windows では、このハンドルはグローバル メモリ ハンドルです (**GlobalAlloc** 関数によって割り当てられます)。 
  
## <a name="see-also"></a>関連項目

- [xlDefineBinaryName](xldefinebinaryname.md)
- [DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

