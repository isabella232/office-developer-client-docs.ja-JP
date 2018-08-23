---
title: '[QuickStyleVariation] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: 数式とテキスト、線、および塗りつぶし色 (またはこれらのプロパティの組み合わせ) の色を使用して値を上書きするかどうかにその図の背景のコントラストを決定します。 値は、0、1、2、4、および 8 のビット単位の OR です。
ms.openlocfilehash: fe6462798b61a0713f98196974876144cf4606e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806140"
---
# <a name="quickstylevariation-cell-quick-style-section"></a>[QuickStyleVariation] セル ([クイック スタイル] セクション)

数式とテキスト、線、および塗りつぶし色 (またはこれらのプロパティの組み合わせ) の色を使用して値を上書きするかどうかにその図の背景のコントラストを決定します。 値は、0、1、2、4、および 8 のビット単位の OR です。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |図形のテキスト、線、または塗りつぶし色 (またはこれらのプロパティの任意の組み合わせ) テーマの特定の背景色を表示したままにするには変わりません。  <br/> |
|1  <br/> |図形のテキスト、線、または塗りつぶし色 (またはこれらのプロパティの任意の組み合わせ) テーマの特定の背景色を表示したままにするには変わりません。  <br/> |
|2  <br/> |背景色が指定されているテーマのに対して表示されたままにするには、必要に応じて図形のテキストの色を変更します。  <br/> |
|4  <br/> |背景色が指定されているテーマのに対して表示されたままにするには、必要に応じて図形の線の色を変更します。  <br/> |
|8  <br/> |背景色が指定されているテーマのに対して表示されたままにするには、必要な場合は、図形の塗りつぶしの色を変更します。  <br/> |
   
## <a name="remarks"></a>注釈

QuickStyleVariation セルを使用して、(たとえば、ネットワーク図などの図形の下端の下のテキスト ボックスは、図形) で表示されている図形ジオメトリの外側である場合、行またはテキストのいずれかの可視性を保証します。 セルの既定値は、0 であり、その動作がアクティブであることを意味します。 その他の値は、セルの動作をトリガーします。
  
QuickStyleVariation 値のセルの色 ([Character] セクション)、FillForegnd、または線の色である場合に、THEMEVAL 関数によって生成された値をオーバーライド (または THEMEVAL を使用してこれら 3 つのプロパティへの直接参照によって生成される ("CharacterColor」)、THEMEVAL("FillColor")、および THEMEVAL("LineColor"))。
  
**CellsU**プロパティを使用して**セル**の要素、またはプログラムから、 **N**属性の値を取得することによって、別の数式の名前によって**QuickStyleVariation** ] セルへの参照を取得して、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |QuickStyleVariation  <br/> |
   
プログラムから、インデックスによって [ **QuickStyleVariation** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
|セル インデックス:  <br/> |**visQuickStyleVariation** <br/> |
   

