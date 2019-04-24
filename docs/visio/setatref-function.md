---
title: SETATREF 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60113
localization_priority: Normal
ms.assetid: 1ecfdb05-2533-470a-006b-e554026944d8
description: ユーザーインターフェイス (UI) またはオートメーションのアクションによって更新された値を別のセルにリダイレクトします。
ms.openlocfilehash: c4f5fe94aba90ce0a69983d6637a5399b6e42707
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326020"
---
# <a name="setatref-function"></a>SETATREF 関数

ユーザーインターフェイス (UI) またはオートメーションのアクションによって更新された値を別のセルにリダイレクトします。 
  
## <a name="syntax"></a>構文

SETATREF (* * *reference* * * [, * * *set_expression* * * [, * * *ignore_eval* * *]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _reference_ <br/> |必須  <br/> |**String** <br/> |更新された値をリダイレクトするセルに対する参照を指定します。  <br/> |
| _set_expression_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |_参照_に割り当てられている式。  <br/> |
| _ignore_eval_ <br/> |省略可能  <br/> |**Boolean** <br/> |TRUE の場合、SETATREF 関数は (0) ゼロに評価されます。FALSE (既定値) の場合、SETATREF 関数は_reference_の値に評価されます。  <br/> |
   
## <a name="remarks"></a>解説

図面ウィンドウでユーザー操作が行われたとき、またはオートメーションメソッドによって、SETATREF 数式を含むセルが更新されると、その値は SETATREF formula (_参照_) で参照されるセルにリダイレクトされます。 SETATREF 関数を含むセルの数式はそのままです。
  
_set_expression_が省略された場合、UI で設定された値またはオートメーションを使用して、参照先セルに設定されます。それ以外の場合は、 _set_expression_の内容が参照先セルに割り当てられます。 これにより、参照先セルに割り当てる前に、新しい値を変更または変換することができます。 
  
SETATREF 関数には次の 2 つの関連する関数があります。 
  
- SETATREFEXPR 関数。 _set_expression_内の新しい値を表すために使用できます。 たとえば、 _set_expression_の SETATREFEXPR () のようになります。 SETATREFEXPR result から2インチを引くために使用できます。 
    
- SETATREFEVAL 関数を使用すると、 _set_expression_の一部を評価し、その結果に置き換える必要があることを示すことができます。 
    
SETATREF 関数は、図面ウィンドウのユーザー操作によって変更できるセルで使用するために設計されています。 次のセルがサポートされています。
  
- [Shape Transform] セクション - [Width]、[Height]、[Angle]、[PinX]、[PinY] の各セル
    
- [Text Transform] セクション - [TxtWidth]、[TxtHeight]、[TxtAngle]、[TxtPinX]、[TxtPinY] の各セル
    
- [1-D Endpoints] セクション - [BeginX]、[BeginY]、[EndX]、[EndY] の各セル
    
- [Controls] セクション - [Controls.X]、[Controls.Y] の各セル
    
- [Shape Data] セクション
    
SETATREF はセルの値が変更された場所を変更するため、イベントの発生に影響します。 セルに SETATREF が含まれている場合、 **FormulaChanged**および**CellChanged**イベントは、SETATREF を含むセルではなく、SETATREF によって参照されているセルに対して発生します。 SETATREF を含むセルに SETATREFEXPR も含まれている場合、function パラメーターが変更されているため、SETATREF を含むセルに対しても**FormulaChanged**イベントが発生します。 
  
SETATREF 関数についてのその他の重要な点は、以下のとおりです。
  
- SETATREF 関数は、他の SETATREF 関数に対し、最大 10 の参照を連鎖させることができます。 
    
- セルには、SETATREF 関数以外の式を含めることができます。1 つのセルに SETATREF を複数使用することもできます。
    
- 図形を接着している場合、Visio は同じシート内で連鎖している SETATREF 参照に従って、参照先のセルに接着する数式を配置します。 
    
- オートメーションは SETATREF 関数を認識して、参照先のセルの連鎖に従います。 
    
- GUARD 同様、SETATREF はシェイプシートの SETF 関数による変更からセルを保護しません。
    
## <a name="example1"></a>例1

図形に [Width] というカスタム プロパティがあり、[Shape Transform] セクションの [Width] セルに次の数式が含まれているとします。
  
= SETATREF (Prop)
  
ユーザーが UI で図形の幅を変更した場合は、新しい値が [図形の変換] セクションの [width] セルではなく、[... width] セルに割り当てられます。[幅] セルの数式は変更されません。 図形データを使用して、図形の幅を設定することもできます。
  
## <a name="example2"></a>例2

Visio ソリューションには階層関係を持つ図形が多く、親図形が移動する際には子図形も移動する必要があります。シェイプシートの SETATREF 関数を使用してこの関係を管理する例を次に示します。 
  
次の数式は子図形の [Shape Transform] セクションに含まれます。また、親図形からのオフセット寸法を追跡する [User.DeltaX] および [User.DeltaY] というユーザー セルを定義します。これにより、親図形が移動する際に子図形も移動することができます。また、子図形が移動する場合にも階層関係を保持することができます。
  
PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX
  
PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY
  
UI を使用して子図形を移動すると、新しい PinX および PinY の値が SETATREFEXPR 関数のパラメーターとして設定されます。 SETATREF 関数は、SETATREFEVAL に含まれている数式を評価し、PinX と PinY をその結果に置き換え、結果として得られた数式を、SETATREF 関数で参照されるユーザーセル (deltax および) に割り当てます。 最後に、SETATREF (deltay) によって返された値が、子図形の pin 位置を計算するために、parentshape のピン位置に追加されます。
  

