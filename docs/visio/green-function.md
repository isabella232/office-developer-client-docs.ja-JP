---
title: GREEN 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251434
localization_priority: Normal
ms.assetid: eccec432-32d3-15c2-06b3-dd02b6313d4c
description: 色の緑のコンポーネントを返します。
ms.openlocfilehash: 04bdadc0fa34dc4f51061d428b9366a433b669a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805518"
---
# <a name="green-function"></a>GREEN 関数

色の緑のコンポーネントを返します。
  
## <a name="syntax"></a>構文

緑 (* **式** *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須  <br/> |**によって異なります** <br/> |(RGB や hsl など) などのユーザー設定の色またはカラー インデックスや色の結果を含むセルへの参照に解決される式のドキュメントのカラー テーブルで色のインデックス。  <br/> |
   
### <a name="return-value"></a>�߂�l

整数型 (Integer)
  
## <a name="remarks"></a>Remarks

戻り値は、0 ~ 255 の範囲、範囲内の数値、またはインデックスを判別するセル参照です。 *式*が有効でない場合は、0 (黒) を返します。 
  
## <a name="example-1"></a>例 1

緑 (Sheet.4!FillForegnd)
  
Sheet.4 について、前景の塗りつぶしの色に関する緑のコンポーネントを返します。
  
## <a name="example-2"></a>例 2

GREEN(11)
  
図面で既定の Visio カラー パレットを使用する場合、128 を返します。Visio カラー パレットでは、インデックス 11 は濃い黄を示します。
  
## <a name="example-3"></a>例 3

GREEN(RGB(10, 20, 30))
  
20 を返します。
  

