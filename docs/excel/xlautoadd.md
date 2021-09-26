---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- xlautoadd function [excel 2007]
ms.localizationpriority: medium
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 574d5f446ec4114cfbf94bea984fb0df92f072f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611218"
---
# <a name="xlautoadd"></a>xlAutoAdd

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
ユーザーが Excel セッション中にアドイン マネージャーを使用して XLL をアクティブ化するたびに、Microsoft Excel によって追加されます。Excel が起動して、あらかじめインストールされたアドインを読み込む際には、この関数は呼び出されません。
  
たとえば、この関数を使用して、アドインが有効になっていることをユーザーに通知するカスタム ダイアログ ボックスの表示、レジストリの読み取りと書き込み、ライセンス情報の確認などができます。
  
Excel では、これらの関数の実装とエクスポートに XLL は必要ありません。
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a>パラメーター

この関数に引数はありません。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

この関数を実装する場合、1 (**int**) を返す必要があります。
  
## <a name="remarks"></a>注釈

アドイン マネージャーが任意のタスクを追加するときに、そのタスクを XLL が実行する必要がある場合は、この関数を使用します。
  
## <a name="example"></a>例

この関数の実装例については、`\SAMPLES\EXAMPLE\EXAMPLE.C` と `\SAMPLES\GENERIC\GENERIC.C` を参照してください。次のコードは、`\SAMPLES\EXAMPLE\EXAMPLE.C` から抜粋しています。
  
```cs
int WINAPI xlAutoAdd(void)
{
    XCHAR szBuf[255];
    wsprintfW((LPWSTR)szBuf, L"Thank you for adding Example.XLL\n"
            L"build date %hs, time %hs",__DATE__, __TIME__);
/* Display a dialog indicating that the XLL was successfully added */
    Excel12f(xlcAlert, 0, 2, TempStr12(szBuf), TempInt12(2));
    return 1;
}
```

## <a name="see-also"></a>関連項目



[xlAutoRemove](xlautoremove.md)


[アドイン マネージャーと XLL インターフェイス関数](add-in-manager-and-xll-interface-functions.md)

