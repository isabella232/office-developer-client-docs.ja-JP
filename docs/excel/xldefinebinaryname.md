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
# <a name="xldefinebinaryname"></a>xlDefineBinaryName

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
**xltypeBigData** **XLOPER**/ **XLOPER12** の永続ストレージを割り当てるために使用します。 定義されているバイナリ名が含まれるデータはブックに保存され、いつでも名前でアクセスできます。 詳細については、「[Excel XLL 開発での既知の問題](known-issues-in-excel-xll-development.md)」の「バイナリ名のスコープ制限」を参照してください。
  
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

