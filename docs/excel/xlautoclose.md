---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- xlautoclose function [excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3cbe1cd879fb5a91d14b38f8a659a7f77d943fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798977"
---
# <a name="xlautoclose"></a>xlAutoClose

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
XLL ファイルが非アクティブになるたびに、Microsoft Excel に呼び出されます。Excel セッションが正常に終了すると、アドインは非アクティブになります。アドインは、Excel セッション中にユーザーによって非アクティブ化される場合があります。この関数はその場合に呼び出されます。
  
関数とコマンドの登録解除、リソースの解放、カスタマイズを元に戻すことなどを XLL が実行できるようするために適切なことではありますが、Excel はこの関数を実装しエクスポートするのに、XLL を必要としません。関数とコマンドを XLL が明示的に登録解除しない場合、**xlAutoClose** 関数を呼び出した後、Excel はこれを実行します。 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a>パラメーター

この関数に引数はありません。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

この関数を実装する場合、1 (**int**) を返す必要があります。
  
## <a name="remarks"></a>注釈

XLL が非アクティブになる、つまりメモリからアンロードされるたびに、Excel は **xlAutoClose** 関数を呼び出します。以下の状況で、XLL は非アクティブになります。 
  
- セッション中にアクティブな場合に、Excel セッションが正常に終了した時点。
    
- Excel セッション中に明示的にアンロードされた場合。
    
- XLL は以下のいくつかの方法でアンロードされる可能性があります。
    
- アドイン マネージャーを使用する。
    
- この DLL の名前を唯一の引数として取る [xlfUnregister](xlfunregister-form-1.md) を呼び出す別の XLL から。 
    
- この DLL の名前を唯一の引数として取る [UNREGISTER](xlfunregister-form-1.md) を呼び出す XLM マクロ シートから。 
    
この関数は、以下を実行します。
  
- XLL が追加した任意のメニューまたはメニュー項目を削除する。
    
- 任意の必要なグローバル クリーンアップを実行する。
    
- 作成された任意の名前、特にエクスポートされた関数の名前を削除する。**REGISTER** に 4 番目の引数が指定されていると、関数の登録が原因で複数の名前が作成される可能性があることに注意してください。 
    
## <a name="example"></a>例

この関数の実装例については、`SAMPLES\EXAMPLE\EXAMPLE.C` ファイルと `SAMPLES\GENERIC\GENERIC.C` ファイルを参照してください。次のコードは、`SAMPLES\GENERIC\GENERIC.C` から抜粋しています。
  
```cs
int WINAPI xlAutoClose(void)
{
   int i;
   XLOPER12 xRes;
//
// This block first deletes all names added by xlAutoOpen or
// xlAutoRegister12. Next, it checks if the drop-down menu Generic still
// exists. If it does, it is deleted using xlfDeleteMenu. It then checks
// if the Test toolbar still exists. If it is, xlfDeleteToolbar is
// used to delete it.
//
// The following code to delete the defined names
// does not work in the current version of Excel. 
// You cannot delete these names once they are Registered.
// The code is left here in case the functionality becomes 
// available in a future version.
//
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgWorksheetFuncs[i][2]));
   for (i = 0; i < g_rgCommandFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgCommandFuncs[i][2]));
//
// Everything else works as documented.
//
   Excel12f(xlfGetBar, &amp;xRes, 3, TempInt12(10), TempStr12(L"Generic"), TempInt12(0));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteMenu, 0, 2, TempNum12(10), TempStr12(L"Generic"));
      // Free the XLOPER12 returned by xlfGetBar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   Excel12f(xlfGetToolbar, &amp;xRes, 2, TempInt12(7), TempStr12(L"Test"));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteToolbar, 0, 1, TempStr12(L"Test"));
      // Free the XLOPER12 returned by xlfGetToolbar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   return 1;
}
```

## <a name="see-also"></a>関連項目



[xlAutoOpen](xlautoopen.md)


[アドイン マネージャーと XLL インターフェイス関数](add-in-manager-and-xll-interface-functions.md)

