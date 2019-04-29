---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- xlfsetname function [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6327ccf2cd18e42c3ef9abe538e6f669e498352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404261"
---
# <a name="xlfsetname"></a>xlfSetName

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
DLL に関連付けられている定義済みの名前を作成および削除するために使用します。
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a>パラメーター

_pxNameText_ (**xltypeStr**)
  
名前の範囲。この名前は、有効な名前に関する Microsoft Excel の通常の制限に準拠する必要があります。
  
_pxNameDefinition_ (**xltypeStr**、**xltypeNum**、**xltypeBool**、**xltypeErr**、**xltypeMulti**、**xltypeSRef**、**xltypeRef**、または **xltypeInt**)
  
(省略可能)。 値、値のセット、セル、または _pxNameText_ として定義されたセルの範囲。 省略した場合は名前が削除されます。 
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

_pxRes _ (**xltypeBool** または **xltypeErr**)
  
操作が成功した場合は TRUE、名前を作成または削除できなかった場合は FALSE を返します。引数の 1 つ以上が無効であれば、#VALUE! を返します。
  
## <a name="remarks"></a>注釈

有効な _pxFunctionText_ 引数を設定した **xlfRegister** を使用して関数またはコマンドが登録されると、Excel は DLL リソースに関連付けた名前を作成します。DLL がアンロードされる場合、これらの名前は [xlfSetName 関数](xlfsetname.md)を使用して削除されなければなりません。ただし、この削除操作は Excel の既知の問題が原因で失敗します。詳細については、「[Excel XLL 開発での既知の問題](known-issues-in-excel-xll-development.md)」を参照してください。
  
### <a name="example"></a>例

`\SAMPLES\GENERIC\GENERIC.C` で、**xlAutoClose** 関数のコードを参照してください。
  
## <a name="see-also"></a>関連項目

- [重要で役に立つ C API XLM 関数](essential-and-useful-c-api-xlm-functions.md)

