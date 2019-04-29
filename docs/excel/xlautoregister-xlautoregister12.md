---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- xlautoregister function [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f043558f3f642001e9ba11ee5b18a2721c3dddfb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421166"
---
# <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
登録対象の関数の戻り値の型と引数の型がない状態で、XLM 関数 **REGISTER**、または C API の同等の [xlfRegister 関数](xlfregister-form-1.md)に対する呼び出しが実行されると、常に Excel は [xlAutoRegister 関数](xlautoregister-xlautoregister12.md)を呼び出します。
  
Excel 2007 以降では、**xlAutoRegister12** 関数が XLL によってエクスポートされている場合、Excel はこの関数を **xlAutoRegister** 関数よりも優先して呼び出します。 
  
Excel では、XLL がこれらいずれかの関数を実装してエクスポートすることは不要です。
  
> [!NOTE]
> **xlAutoRegister**/ **xlAutoRegister12** が引数の型と戻り値の型を指定しないで関数を登録しようとすると、最終的にコール スタックがオーバーフローし、Excel がクラッシュする原因となる再帰呼び出しのループが発生します。 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>パラメーター

 _pxName_ (**xltypeStr**)
  
登録される XLL 関数の名前です。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

この関数は、**xlfRegister** 関数を使用して XLL 関数 _pxName_ を登録を試行した結果を返します。指定した関数が XLL ファイルのエクスポートの 1 つでない場合、関数は **#VALUE!** エラーを返すか、Excel が **#VALUE!** と解釈する **NULL** を返す必要があります。
  
## <a name="remarks"></a>注釈

**xlAutoRegister** の実装では、エクスポートする XLL ファイルの関数とコマンドの内部リストで大文字小文字を区別する検索を実行して、渡された名前との一致を検索する必要があります。関数またはコマンドが見つかった場合、**xlAutoRegister** は **xlfRegister** 関数を使用し、Excel に関数の戻り値の型と引数の型、および関数に関するその他の必要情報を指示する文字列を指定して、登録を試行する必要があります。これは、**xlfRegister** に対する呼び出しが返された場合にも、Excel に返す必要があります。関数が正常に登録された場合、**xlfRegister** は関数の登録 ID を含む **xltypeNum** 値を返します。 
  
### <a name="example"></a>例

この関数の実装例については、ファイル `SAMPLES\EXAMPLE\EXAMPLE.C` を参照してください。 
  
## <a name="see-also"></a>関連項目



[REGISTER](xlfregister-form-1.md)
  
[UNREGISTER](xlfunregister-form-1.md)

