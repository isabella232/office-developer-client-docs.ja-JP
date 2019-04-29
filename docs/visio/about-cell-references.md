---
title: セルの参照について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251827
localization_priority: Normal
ms.assetid: e6a9aceb-90d7-fb53-eaf4-416a1ae2a98b
description: シェイプシートのセルの参照を使用すると、数式間の相互依存を作成できます。セルの参照によって、別のセルの値を基にセルの値を計算できます。たとえば、図形の [Width] セルに、図形の [Height] セルの値を参照して図形の幅を計算する数式が含まれている場合、図形の高さを変更すると、高さに比例して図形の幅も変更されます。
ms.openlocfilehash: a92bcc560c535dc012ec5cb79db72250e78364c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409805"
---
# <a name="about-cell-references"></a>セルの参照について

シェイプシートのセルの参照を使用すると、数式間の相互依存を作成できます。セルの参照によって、別のセルの値を基にセルの値を計算できます。たとえば、図形の [Width] セルに、図形の [Height] セルの値を参照して図形の幅を計算する数式が含まれている場合、図形の高さを変更すると、高さに比例して図形の幅も変更されます。
  
セルの数式では、同じ図形のセル、または図面やページなどの他のオブジェクトのセルを参照できるので、Microsoft Visio では特定のセルの値を基にして別のセルの値を計算できます。
  
## <a name="what-cell-references-can-include"></a>セルの参照に含められるもの

セルの参照は、図形の識別子 (ID) または名前を含むことができます。 図形に名前があってもなくても、そのID を用いてページ上にある全ての図形をいつでも参照できます。 図形に名前が付いていない場合、図形の既定の名前は Sheet です。 図形の IDが *i*であるところの*i*。 図形が作成されると割り当てられる ID は、その図形を別のぺ―ジまたは別のドキュメントに移動しない限り変更しません。 ページ上に同じ名前の図形が複数ある場合、割り当てられた ID を含む必要があります。 
  
## <a name="cell-reference-syntax-and-examples"></a>セル参照の構文と例

使用する構文、および名前によって図形を参照できるかどうかは、2 つのオブジェクトの関係によって決まります。次の一般的な規則が適用されます。
  
- 数式を編集している図形と参照先となる図形が同等なものである場合、図形を名前で参照できます。この同等の図形がグループである場合、グループを名前で参照することはできますが、そのメンバーは参照できません。さらに、図形の親または図形の親と同等な図形は名前で参照できません。
    
- Sheet.ID 構文を使用すると、図形がグループに属しているかどうか、または図形がある図形の親であるかどうかに関係なく、ページ上の図形をどれでも参照できます。
    
- 特殊な文字を含む名前は、一重引用符で囲む必要があります。特殊な名前の一部に一重引用符を使用する場合は、その引用符の前に一重引用符を付けます。
    
|**セルを参照するには**|**次の構文を使用します**|**例**|
|:-----|:-----|:-----|
|同じ図形  <br/> | CellName  <br/> | Width  <br/> |
| 図形、グループまたはガイド  <br/> | Shapename!CellName  <br/> | Star!Angle  <br/> |
| 同じレベルに同じ名前を持つ図形が複数あるところの図形、グループまたはガイド  <br/> | Shapename.ID!CellName  <br/> | Executive.2!Height  <br/> |
| インデックス付きの行を含む名前付きの列  <br/> | Section.Column[index]  <br/> | Char.Font[3]  <br/> |
| インデックス付きの行を含む名前の付いていない列  <br/> | Section.ColumnIndex  <br/> | Scratch.A5  <br/> |
| すべての図形、ページ、マスターまたはスタイル  <br/> | Sheet.ID!CellName  <br/> | Sheet.8!FillForegnd  <br/> |
| マスター  <br/> | Masters[MasterName]!SheetName!CellReference  <br/> | Masters[Gear]!Shaft!Geometry1.X1  <br/> |
| オブジェクトが存在するマスター ページまたはページ  <br/> | ThePage!CellReference  <br/> | ThePage!User.Vanishing_Point  <br/> |
| ドキュメント内の別のページ  <br/> | Pages[PageName]!SheetName!CellReference  <br/> | Pages[Page-3]!Sheet.4!BeginX  <br/> |
| スタイル  <br/> | Styles!SheetName!CellReference  <br/> | Styles!Manager!LineColor  <br/> |
| ドキュメント  <br/> | TheDoc!CellReference  <br/> | TheDoc!PreviewQuality  <br/> |
| 非標準の名前付きの図形、ページ、マスター、ドキュメントまたはスタイル。  <br/> | 'Sheetname'!CellName  <br/> | '1-D'!LineColor  <br/> |
   

