---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5b58b71dc4f2441448eb3e0dac2c3c5763675927
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310428"
---
# <a name="showoptions"></a>ShowOptions

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
ユーザーから情報を収集するためのモーダル ダイアログ ボックスを表示します。このエントリ ポイントは、**[Excel のオプション]** ダイアログ ボックス (**[数式]** セクションの下にある **[詳細設定]** カテゴリ内) で、選択したクラスター コネクタの **[クラスターの種類]** ボックスの隣にある **[オプション]** ボタンをクリックすると呼び出されます。クラスター コネクタで、独自のオプション ダイアログのインターフェイスを実装するとともに、レジストリまたは他の場所に関連データを格納する必要があります。オプションは、クラスター コネクタ内部にあります。Excel には認識されません。 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a>パラメーター

_hWndParent_
  
> Excel ウインドウへのハンドル。
    
## <a name="return-value"></a>戻り値

ダイアログ ボックスが表示された場合は **xlHpcRetSuccess**、表示されなかった場合は **xlHpcRetCallFailed**。 
  
## <a name="remarks"></a>注釈

クラスター コネクタでは、使用するクラスター サーバーなどの情報をユーザーから取得するために、このダイアログ ボックスを使用できます。
  
## <a name="see-also"></a>関連項目

- [Excel クラスター コネクタ関数](excel-cluster-connector-functions.md)

