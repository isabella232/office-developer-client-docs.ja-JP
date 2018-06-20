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
description: テキスト行を超えている maximumwidth 図形で構成されたテキストの高さを返しません。
ms.openlocfilehash: 9a80dafcf80a1dcba968a0f60465aae4e2a2758b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806629"
---
# <a name="textheight-function"></a>TEXTHEIGHT 関数

テキスト行を超えている_maximumwidth_図形で構成されたテキストの高さを返しません。 
  
## <a name="syntax"></a>構文

TEXTHEIGHT (* **なります。[Thetext]* * * * * *[] maximumwidth* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _なります! テキスト_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |セルへの参照では、接続先の図形の [thetext] という名前です。  _なります!_ テキストを取得する図形の名前です。  <br/> |
| _maximumwidth_ <br/> |省略可能  <br/> |**数値** <br/> |テキスト ブロックの最大幅を指定します。  <br/> |
   
### <a name="return-value"></a>�߂�l

String
  
## <a name="remarks"></a>注釈

戻り値として、テキストの前後のスペースを含む高さ、行間隔、およびテキスト ブロックの上下の余白が返されます。この関数は、通常、格納するテキストのサイズに合わせて図形の高さを調整する場合に使用します。
  
## <a name="example"></a>例

TEXTHEIGHT(TheText,(Width - 0.5 in)) 
  
図形の幅から 0.5 インチ差し引いた幅で折り返した場合の、テキストの高さを返します。 
  

