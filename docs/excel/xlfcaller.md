---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- xlfcaller function [excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 92d2d1877d7b315d178ef1fa36b47bd5f9f8e661
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798969"
---
# <a name="xlfcaller"></a>xlfCaller

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
現在実行中の DLL コマンドまたは関数を呼び出したセル、セルの範囲、メニューのコマンド、ツールバーのツール、またはオブジェクトに関する情報を返します。
  
|**呼び出し元のコード**|**返される値**|
|:-----|:-----|
|DLL  <br/> |登録 ID。  <br/> |
|単一のセル  <br/> |単一セルの参照。  <br/> |
|複数セルの配列数式  <br/> |複数セルの参照。  <br/> |
|条件付き書式設定式  <br/> |書式設定の条件が適用されているセルへの参照。  <br/> |
|メニュー  <br/> | 4 つの要素の単一行配列  <br/>  バーの ID。  <br/>  メニューの位置。  <br/>  サブメニューの位置。  <br/>  コマンドの位置。  <br/> |
|ツールバー  <br/> | 2 つの要素の単一行配列  <br/>  組み込みツールバーの場合はツールバー番号、カスタム ツールバーの場合はツールバー名。  <br/>  ツールバー上の位置。  <br/> |
|グラフィック オブジェクト  <br/> |オブジェクトの識別子 (オブジェクト名)。  <br/> |
|xlcOnEnter、ON.ENTER、イベント トラップに関連付けられたコマンド  <br/> |入力される 1 つまたは複数のセルへの参照。  <br/> |
|xlcOnDoubleclick、ON.DOUBLECLICK、イベント トラップに関連付けられたコマンド  <br/> |ダブルクリックされたセル (必ずしもアクティブなセルではありません)。  <br/> |
|Auto_Open、AutoClose、Auto_Activate または Auto_Deactivate マクロ  <br/> |呼び出し元シートの名前。  <br/> |
|この一覧にない他のメソッド  <br/> |#REF! エラー。  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

戻り値は、**XLOPER**/ **XLOPER12** データ型の **xltypeRef**、**xltypeSRef**、**xltypeNum**、**xltypeStr**、**xltypeErr**、または **xltypeMulti** です。これらの型のうちの 3 つは割り当て済みのメモリを指すため、必要がなくなったら、必ず [xlFree function](xlfree.md) の呼び出しで、**xlfCaller** の戻り値を解放する必要があります。 
  
**XLOPER**/ **XLOPER12** の詳細については、「[Excel でのメモリ管理](memory-management-in-excel.md)」を参照してください。
  
## <a name="remarks"></a>注釈

この関数は、DLL/XLL ワークシート関数から呼び出し可能な唯一の非ワークシート関数です。その他の XLM 情報関数は、コマンドまたはマクロ シート同等の関数からのみ呼び出すことができます。
  
## <a name="example"></a>例

 `\SAMPLES\EXAMPLE\EXAMPLE.C`。この関数はコマンド マクロ (xlcSelect) を呼び出し、マクロ シートから呼び出された場合にのみ正しく動作します。
  
```cs
short WINAPI CallerExample(void)
{
   XLOPER12 xRes;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>関連項目



[重要で役に立つ C API XLM 関数](essential-and-useful-c-api-xlm-functions.md)

