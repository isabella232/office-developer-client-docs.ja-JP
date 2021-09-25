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
ms.localizationpriority: medium
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 443b6511e0935737187994bf0224bd80b84ada21
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621354"
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

