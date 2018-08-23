---
title: LOC 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251455
localization_priority: Normal
ms.assetid: 7db7a8ed-50a9-8495-b978-42a2fddb466a
description: 1 つの図形のローカル座標で定義されているポイントを取得し、数式に関連付けられている図形のローカル座標で表された点を返します。
ms.openlocfilehash: 196e2c92ea6ab410b6ecca9767b68605e4eb4d30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805738"
---
# <a name="loc-function-visioshapesheet"></a>LOC 関数 (VisioShapeSheet)

1 つの図形のローカル座標で定義されているポイントを取得し、数式に関連付けられている図形のローカル座標で表された点を返します。 
  
## <a name="syntax"></a>構文

LOC (* **ポイント** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _ポイント_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 1 つの図形のローカル座標に定義されている点を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

String
  
## <a name="remarks"></a>注釈

ローカル座標は図形の選択範囲の左下隅から測定されます。両方の図形は、同じページになければなりません。
  
## <a name="example"></a>例

LOC (サーフェス (Sheet.5!Sheet.5 [locpinx]![Locpiny])) 
  
この式では、PNT 関数が Sheet.5 にある一連のローカル座標を点に変換します (Sheet.5 は同じ図面ページ上にある別の図形です)。次に LOC 関数は、この点を、現在の図形のローカル座標系で相当する点に変換します。このとき、現在の図形の選択範囲の左下隅を原点として変換が行われます。 
  
Sheet.5 の 5 は図形の ID 番号であり、これは [**図形の名前**] ダイアログ ボックス ([**開発者用**] タブ) に表示されます。 
  

