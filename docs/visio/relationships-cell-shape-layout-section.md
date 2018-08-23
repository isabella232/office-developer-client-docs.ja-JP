---
title: '[Relationships] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80005
localization_priority: Normal
ms.assetid: 4168cd98-9674-1233-254f-0afe81b7245b
description: コンテナー、リスト、引き出し、および図形どうしの関係を格納します。
ms.openlocfilehash: c3410ad15581ff1704d7a43dd7ed5fa193f668b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806184"
---
# <a name="relationships-cell-shape-layout-section"></a>[Relationships] セル ([図形レイアウト] セクション)

コンテナー、リスト、引き出し、および図形どうしの関係を格納します。 
  
## <a name="remarks"></a>注釈

 Microsoft Visio では、この図形に関連するリレーションシップを保存するのには関係のセルを使用します。 DEPENDSON 関数は、表示されているパラメーターを使用して一連は、次の表に示すように、この図形では、リレーションシップを表現する使用されます。 
  
|**最初のパラメーター**|**追加パラメーター**|
|:-----|:-----|
|1  <br/> |このコンテナーのメンバーである図形。  <br/> |
|2  <br/> |このリストのメンバーである図形。  <br/> |
|3  <br/> |この図形に関連付けられた引き出し。  <br/> |
|4  <br/> |この図形がメンバーとして属しているコンテナー。  <br/> |
|5  <br/> |このリスト項目がメンバーとして属しているリスト。  <br/> |
|6  <br/> |この引き出しに関連付けられた図形。  <br/> |
|7  <br/> |この図形が配置されている左端のコンテナー。  <br/> |
|8  <br/> |この図形が配置されている右端のコンテナー。  <br/> |
|9  <br/> |この図形が配置されている上端のコンテナー。  <br/> |
|10  <br/> |この図形が配置されている下端のコンテナー。  <br/> |
|11  <br/> |このリストが重なっているリスト。  <br/> |
   
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Relationships] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Relationships  <br/> |
   
プログラムから、インデックスによって [Relationships] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLORelationships** <br/> |
   

