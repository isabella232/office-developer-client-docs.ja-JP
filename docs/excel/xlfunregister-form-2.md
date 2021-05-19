---
title: xlfUnregister (形式 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8bf1151e1ba4c165e784b88dce80096a2eaa62de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419906"
---
# <a name="xlfunregister-form-2"></a>xlfUnregister (形式 2)

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel から呼び出された DLL コマンドまたは XLL コマンドから呼び出すことができます。これは、**UNREGISTER** を Excel XLM マクロ シートから呼び出すのと同等です。 
  
**xlfUnregister** 関数は、次の 2 つの形式で呼び出すことができます。 
  
- 形式 1: 個々のコマンドや関数の登録を解除します。
    
- 形式 2: XLL のアンロードと非アクティブ化を行います。
    
形式 2 で呼び出されると、この関数は DLL やコード リソースの完全なアンロードを強制します。別のマクロで現在使われていても、DLL 内のすべての関数の登録を解除します。関数の使用について考慮されません。この関数は **xlAutoClose** を呼び出してから、DLL 内のすべての関数の登録を解除します。
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>パラメーター

_pxModuleText_ (**xltypeStr**)
  
DLL の名前。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

成功した場合は、**TRUE** (**xltypeBool**) が返されます。失敗した場合は、**FALSE** が返されます。
  
## <a name="remarks"></a>注釈

> [!NOTE] 
> この形式の関数を [xlAutoClose](xlautoclose.md) の実装から呼び出して、1 つの単純な関数の呼び出しにより DLL のすべてのリソースの登録を解除しようとしないでください。 これにより、**xlAutoClose** の再帰呼び出しがなされスタック オーバーフローになります。 
  
### <a name="remember-to-delete-names"></a>名前を削除することを忘れないでください

_pxFunctionText_ 引数を **xlfRegister** に指定する場合は、DLL の関数とコマンドの登録時に、それぞれについて 2 つ目の引数を省略して **xlfSetName** を呼び出し、関数が関数ウィザードに表示されないように名前を明示的に削除する必要があります。詳細については、「[Excel アドイン (XLL) 開発における既知の問題](known-issues-in-excel-xll-development.md)」を参照してください。
  
## <a name="see-also"></a>関連項目

- [xlfRegister (形式 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (形式 1)](xlfunregister-form-1.md)
- [重要で役に立つ C API XLM 関数](essential-and-useful-c-api-xlm-functions.md)

