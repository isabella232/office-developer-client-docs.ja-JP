---
title: LOC 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251455
ms.localizationpriority: medium
ms.assetid: 7db7a8ed-50a9-8495-b978-42a2fddb466a
description: 1 つの図形のローカル座標で定義された点を取得し、数式に関連付けられた図形のローカル座標で表される同等の点を返します。
ms.openlocfilehash: 82a399a3e50aa94a9d158260bd9292a026af4017
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565976"
---
# <a name="loc-function-visioshapesheet"></a>LOC 関数 (VisioShapeSheet)

1 つの図形のローカル座標で定義された点を取得し、数式に関連付けられた図形のローカル座標で表される同等の点を返します。 
  
## <a name="syntax"></a>構文

LOC(** *point* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _point_ <br/> |必須  <br/> |**String** <br/> | 1 つの図形のローカル座標に定義されている点を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

ローカル座標は図形の選択範囲の左下隅から測定されます。両方の図形は、同じページになければなりません。
  
## <a name="example"></a>例

LOC(PNT(Sheet.5!LocPinX、Sheet.5!LocPinY)) 
  
この式では、PNT 関数が Sheet.5 にある一連のローカル座標を点に変換します (Sheet.5 は同じ図面ページ上にある別の図形です)。次に LOC 関数は、この点を、現在の図形のローカル座標系で相当する点に変換します。このとき、現在の図形の選択範囲の左下隅を原点として変換が行われます。 
  
Sheet.5 の 5 は図形の ID 番号であり、これは [**図形の名前**] ダイアログ ボックス ([**開発者用**] タブ) に表示されます。 
  

