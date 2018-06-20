---
title: '[LangID] セル ([Annotation] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60048
localization_priority: Normal
ms.assetid: b6f5ea5e-b350-0817-d631-f059b9b95c23
description: コメントの記入に使用した言語を示します。
ms.openlocfilehash: 0de5ed8136a3fb1bbdca9fea0ebb5894e62cf907
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805655"
---
# <a name="langid-cell-annotation-section"></a>[LangID] セル ([Annotation] セクション)

コメントの記入に使用した言語を示します。
  
> [!NOTE]
> このセルは、Microsoft Visio 2013 で .vsd ファイルを開くときにのみ、または .vsd ファイルの形式で .vsdx ファイルを保存するときにコメントを追跡するために使用されます。 Visio 2013 で .vsdx のドキュメント内のコメントを追跡するためには使用されません。 
  
## <a name="remarks"></a>備考

この値は、ロケール ID (LCID) のコメントが入力されたときに、言語バーでアクティブになっている言語です。 Microsoft Office アプリケーションでサポートされる言語のリストは、 [[doclangid]](doclangid-cell-document-properties-section.md)セル ([ドキュメント プロパティ] セクションで) のトピックを参照してください。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって langid] セルへの参照を取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Annotation.LangID [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [langid] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionAnnotation** <br/> |
| 行インデックス:  <br/> |**visRowAnnotation** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visAnnotationLangID** <br/> |
   

