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
description: 色の緑コンポーネントを返します。
ms.openlocfilehash: 0412e4519c2964b05d7663805d7773e8dc5deaab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360208"
---
# <a name="green-function"></a>GREEN 関数

色の緑コンポーネントを返します。
  
## <a name="syntax"></a>構文

緑 (* **式** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須  <br/> |**さまざま** <br/> |ドキュメントのカラーテーブルにある色のインデックス、ユーザー設定の色に解決される式 (RGB や HSL など)、またはカラーインデックスや色の結果を含むセルへの参照を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>解説

戻り値は、0 ～ 255 の数値、またはインデックスを判別するセル参照になります。 *式*が無効な場合は、0 (黒) を返します。 
  
## <a name="example-1"></a>例 1

緑 (Sheet. 4![fillforegnd]
  
Sheet.4 について、前景の塗りつぶしの色に関する緑のコンポーネントを返します。
  
## <a name="example-2"></a>例 2

緑 (11)
  
図面で既定の Visio カラー パレットを使用する場合、128 を返します。Visio カラー パレットでは、インデックス 11 は濃い黄を示します。
  
## <a name="example-3"></a>例 3

GREEN(RGB(10, 20, 30))
  
20 を返します。
  

