---
title: TEXTHEIGHT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251504
localization_priority: Normal
ms.assetid: 5a10892f-c8fa-c127-2f5a-564009ce5411
description: テキスト行が最大幅を超えない図形の構成されたテキストの高さを返します。
ms.openlocfilehash: 7455f58f14f9a4a0ae1fcd5375dba5d5860d3852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427410"
---
# <a name="textheight-function"></a>TEXTHEIGHT 関数

テキスト行が最大幅を超えない図形内の構成されたテキストの高さを  _返します_。 
  
## <a name="syntax"></a>構文

TEXTHEIGHT(** *shapename!TheText* ** *** [,maximumwidth]* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |必須  <br/> |**String** <br/> |ターゲットとなる図形の [TheText] セルに対する参照を指定します。  _shapename!_ は、テキストを取得する図形の名前です。  <br/> |
| _maximumwidth_ <br/> |省略可能  <br/> |**数値型 (Numeric)** <br/> |テキスト ブロックの最大幅を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

戻り値として、テキストの前後のスペースを含む高さ、行間隔、およびテキスト ブロックの上下の余白が返されます。この関数は、通常、格納するテキストのサイズに合わせて図形の高さを調整する場合に使用します。
  
## <a name="example"></a>例

TEXTHEIGHT(TheText,(Width - 0.5 in)) 
  
図形の幅から 0.5 インチ差し引いた幅で折り返した場合の、テキストの高さを返します。 
  

