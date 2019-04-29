---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- xlautoremove function [excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8bd2d44883b1820be42b82d4fe4794fa29caab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425478"
---
# <a name="xlautoremove"></a>xlAutoRemove

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
ユーザーが Excel セッション中にアドイン マネージャーを使用して XLL を非アクティブ化すると、Excel によって呼び出されます。アドインがインストールされている状態で Excel セッションが終了するときには、正常終了でも異常終了でも、この関数は呼び出されません。
  
たとえばこの関数を使用して、アドインが無効になっていることをユーザーに通知するカスタム ダイアログ ボックスを表示したり、レジストリの読み取りと書き込みを行ったりすることができます。
  
Excel では、これらの関数の実装とエクスポートに XLL は必要ありません。 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a>パラメーター

この関数に引数はありません。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

この関数を実装する場合、1 (**int**) を返す必要があります。
  
## <a name="remarks"></a>注釈

アドイン マネージャーによってタスクが削除されたときに XLL がそのタスクを完了する必要がある場合は、この関数を使用します。
  
## <a name="example"></a>例

この関数の実装例については、`\SAMPLES\EXAMPLE\EXAMPLE.C` ファイルと `\SAMPLES\GENERIC\GENERIC.C` ファイルを参照してください。次のコードは、`\SAMPLES\EXAMPLE\EXAMPLE.C` から抜粋しています。
  
```cs
int WINAPI xlAutoRemove(void)
{
/* Display a dialog box indicating that the XLL was successfully removed */
   Excel12f(xlcAlert, 0, 2,
      TempStr12(L"Thank you for removing Example.XLL!"),
      TempInt12(2));
   return 1;
}
```

## <a name="see-also"></a>関連項目



[xlAutoAdd](xlautoadd.md)


[アドイン マネージャーと XLL インターフェイス関数](add-in-manager-and-xll-interface-functions.md)

