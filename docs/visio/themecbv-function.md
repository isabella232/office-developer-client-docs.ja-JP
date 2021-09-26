---
title: THEMECBV 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: 引数として渡される色 (数値) が、アクティブなテーマのグラデーション設定に格納されている指定された濃色または濃色の値によって変更された、ドキュメントのカラー パレット内のインデックスを表す RGB 値または整数を返します。
ms.openlocfilehash: 1d9a95aedee2f04e72bd4868ddfaec149c872b62
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603331"
---
# <a name="themecbv-function"></a>THEMECBV 関数

引数として渡される色 (数値) が、アクティブなテーマのグラデーション設定に格納されている指定された濃色または濃色の値によって変更された、ドキュメントのカラー パレット内のインデックスを表す RGB 値または整数を返します。 
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2013
 
  
## <a name="syntax"></a>構文

 **THEMECBV**( _color_,  _gradient_stop_number_)
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |必須  <br/> |**数値** <br/> |ドキュメントのカラー パレット内のインデックスを表す数値。  <br/> |
| _gradient_stop_number_ <br/> |必須かどうか  <br/> |**数値** <br/> |色に適用する、アクティブなテーマのグラデーションの設定に格納された、グラデーションの分岐点 (濃淡または網かけ)。  <br/> |
   
## <a name="return-value"></a>戻り値

 **数値**
  
## <a name="remarks"></a>注釈

> [!NOTE]
> THEMECBV 関数は、図形に割り当てられた QuickStyle にグラデーションが設定されていない場合、引数として渡される色には何もしません。 
  
テーマのグラデーション設定は、"明るくなる" (濃淡) または "濃淡" (日陰) に対応する一連の番号付きグラデーションストップです。 これらの暗さと明るさは、グラデーションの色効果を作成するために、基本色に適用されます。
  
**THEMECBV** 関数は、カラー入力を使用して、指定のグラデーションの分岐点の濃淡または網かけによって変更された後の色を出力します。 現在のクイック スタイルにグラデーションの塗りつぶしが含まれている場合、色や色合いはテーマの定義から取得されます。 アクティブなクイック スタイルでグラデーションの塗りつぶしが指定されていない場合、または図形にテーマが設定されていない場合、この数式によって最初の引数に渡された色が返されます。 
  
## <a name="example"></a>例

 `THEMECBV(FillForegnd, 5)`
  
[**FillForegnd**] セルで指定した色へのグラデーションの、グラデーションの 5 番目の分岐点に、濃淡または網かけを適用することで作成された色を返します。 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
グラデーションの 2 番目の分岐点を赤の基本色に適用することで作成された、赤の網かけまたは濃淡が返されます。
  

