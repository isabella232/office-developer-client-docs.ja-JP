---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- xlautoopen function [excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bf02f71458f2f4d8514f69a6b6f0921b5318303a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406648"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
すべての有効な XLL によって実装およびエクスポートされる必要があるコールバック関数。XLL 関数とコマンドの登録、データ構造の初期化、ユーザー インターフェイスのカスタマイズなどを行う場合には、**xlAutoOpen** 関数を使用することをお勧めします。 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>パラメーター

この関数に引数はありません。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

この関数を実装する場合、1 (**int**) を返す必要があります。
  
## <a name="remarks"></a>注釈

Microsoft Excel は、XLL がアクティブになると常に **xlAutoOpen** を呼び出します。以下の状況で、XLL はアクティブになります。 
  
- 正常終了した前回の Excel セッションでアクティブであった場合、Excel セッションの開始時。
    
- Excel セッション中に読み込まれた場合。
    
- XLL は以下のいくつかの方法で読み込むことができます。
    
- **[ファイル]** メニューの **[開く]** を選択する (Excel のバージョンが XLL 読み込みのこの方法をサポートしている場合)。 
    
- アドイン マネージャーを使用する。
    
- この DLL の名前を唯一の引数として [xlfRegister](xlfregister-form-1.md) を呼び出す別の XLL から。 
    
- この DLL の名前を唯一の引数として [REGISTER](xlfregister-form-1.md) を呼び出す XLM マクロ シートから。 
    
- アドインが、Excel セッション中に非アクティブにされてから再度アクティブにされる場合、この関数は再アクティブ化のときに呼び出されます。
    
### <a name="example"></a>例

この関数の実装例については、`SAMPLES\EXAMPLE\EXAMPLE.C` ファイルと `SAMPLES\GENERIC\GENERIC.C` ファイルをご覧ください。
  
## <a name="see-also"></a>関連項目



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[アドイン マネージャーと XLL インターフェイス関数](add-in-manager-and-xll-interface-functions.md)

