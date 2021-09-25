---
title: RED 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251487
ms.localizationpriority: medium
ms.assetid: a95fd86d-ebc1-66b6-e7d9-9c8ea84d23ab
description: 色の赤いコンポーネントを返します。
ms.openlocfilehash: 37d54cb5cb35bb285b92ab31eea8482709410911
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623139"
---
# <a name="red-function"></a>RED 関数

色の赤いコンポーネントを返します。 
  
## <a name="syntax"></a>構文

RED(** *式* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須かどうか  <br/> |**さまざま** <br/> |引数として、図面のカラー テーブルにある色のインデックス、ユーザー設定の色を返す式 (RGB や HSL など)、またはカラー インデックスや色の結果を含むセルへの参照を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

番号
  
## <a name="remarks"></a>注釈

戻り値は、0 ～ 255 の数値、またはインデックスを判別するセル参照になります。 式  _が_ 無効な場合、この関数は 0 (黒) を返します。 
  
## <a name="example-1"></a>例 1

RED(22)
  
図面が既定の Microsoft Office Visio カラー パレットを使用する場合、51 を返します。Visio カラー パレットでは、インデックス 22 は濃い灰色を示します。
  
## <a name="example-2"></a>例 2

RED(Char.Color)
  
現在のフォントの色について、赤のコンポーネントの値を返します。
  
## <a name="example-3"></a>例 3

RED(RGB(10, 20, 30))
  
10 を返します。
  

