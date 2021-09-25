---
title: GREEN 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251434
ms.localizationpriority: medium
ms.assetid: eccec432-32d3-15c2-06b3-dd02b6313d4c
description: 色の緑のコンポーネントを返します。
ms.openlocfilehash: fa80526aebc21fc227f54f6c6bb25d397a46b5a1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554713"
---
# <a name="green-function"></a>GREEN 関数

色の緑のコンポーネントを返します。
  
## <a name="syntax"></a>構文

GREEN(** *expression* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須かどうか  <br/> |**さまざま** <br/> |ドキュメントの色テーブル内の色のインデックス、カスタムの色 (RGB や HSL など) に解決する式、または色インデックスまたは色の結果を含むセルへの参照。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>注釈

戻り値は、0 ～ 255 の数値、またはインデックスを判別するセル参照になります。 式  *が*  無効な場合は、0 (黒) を返します。 
  
## <a name="example-1"></a>例 1

GREEN(Sheet.4!FillForegnd)
  
Sheet.4 について、前景の塗りつぶしの色に関する緑のコンポーネントを返します。
  
## <a name="example-2"></a>例 2

GREEN(11)
  
図面で既定の Visio カラー パレットを使用する場合、128 を返します。Visio カラー パレットでは、インデックス 11 は濃い黄を示します。
  
## <a name="example-3"></a>例 3

GREEN(RGB(10, 20, 30))
  
20 を返します。
  

