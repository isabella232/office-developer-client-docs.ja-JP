---
title: THEMECBV 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: グラデーションのテーマの設定に格納されている指定の濃淡または網掛けの値を引数として渡されたカラー (番号) が変更されて、RGB 値またはドキュメントのカラー パレットのインデックスを表す整数を返します。
ms.openlocfilehash: 878da505a840234445d3e16d3b8a68e31eaf5fda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806649"
---
# <a name="themecbv-function"></a>THEMECBV 関数

グラデーションのテーマの設定に格納されている指定の濃淡または網掛けの値を引数として渡されたカラー (番号) が変更されて、RGB 値またはドキュメントのカラー パレットのインデックスを表す整数を返します。 
  
## <a name="version-information"></a>バージョン情報

Visio 2013 のバージョンが追加されます。 
  
## <a name="syntax"></a>構文

 **THEMECBV**(_カラー_、 _gradient_stop_number_)
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |必須  <br/> |**番号** <br/> |ドキュメントのカラー パレット内のインデックスを表す数値。  <br/> |
| _gradient_stop_number_ <br/> |必須  <br/> |**番号** <br/> |色に適用する、アクティブなテーマのグラデーションの設定に格納された、グラデーションの分岐点 (濃淡または網かけ)。  <br/> |
   
## <a name="return-value"></a>�߂�l

 **番号**
  
## <a name="remarks"></a>備考

> [!NOTE]
> THEMECBV 関数では、図形に割り当てられている QuickStyle でグラデーションを設定していない場合、引数として渡された色にしません。 
  
テーマでグラデーションの設定は、一連の「稲妻」(濃淡) と「暗く」(網掛け) に対応する番号付きのグラデーション終了位置です。 これらの網掛けまたは濃淡は、色のグラデーション効果を作成する基本の色に適用されます。
  
**THEMECBV**関数はカラー入力し、指定したグラデーションの分岐点の網掛けまたは濃淡で変更された後に、色を出力します。 濃淡と網掛けは、現在のクイック スタイルには、グラデーションの塗りつぶしが含まれている場合は、テーマの定義から取得されます。 アクティブなクイック スタイルにグラデーションの塗りつぶしまたは図形にテーマなしに設定が指定しない場合、この数式は、最初の引数で渡されたカラーを単に返します。 
  
## <a name="example"></a>例

 `THEMECBV(FillForegnd, 5)`
  
**FillForegnd** ] セルに指定した色にグラデーションの 5 番目のグラデーション終了位置の網掛けまたは濃淡を適用することによって作成された色を返します。 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
グラデーションの 2 番目の分岐点を赤の基本色に適用することで作成された、赤の網かけまたは濃淡が返されます。
  

