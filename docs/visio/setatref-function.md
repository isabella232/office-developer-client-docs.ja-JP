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
description: ユーザー インターフェイス (UI) またはオートメーションのアクションに起因する更新された値を別のセルにリダイレクトします。
ms.openlocfilehash: c4f5fe94aba90ce0a69983d6637a5399b6e42707
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416805"
---
# <a name="setatref-function"></a>SETATREF 関数

ユーザー インターフェイス (UI) またはオートメーションのアクションに起因する更新された値を別のセルにリダイレクトします。 
  
## <a name="syntax"></a>構文

SETATREF(** *reference* ** [, ** *set_expression* ** [, **** ignore_eval ** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _reference_ <br/> |必須  <br/> |**String** <br/> |更新された値をリダイレクトするセルに対する参照を指定します。  <br/> |
| _set_expression_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |参照に割り当てられている  _式_ です。  <br/> |
| _ignore_eval_ <br/> |省略可能  <br/> |**Boolean** <br/> |TRUE の場合、SETATREF 関数は (0) ゼロに評価されます。FALSE (既定値) の場合、SETATREF 関数は参照の値に評価  _されます_。  <br/> |
   
## <a name="remarks"></a>注釈

図面ウィンドウまたはオートメーション メソッドのユーザー アクションによって、Microsoft Visio が SETATREF 数式を含むセルを更新すると、値は SETATREF 数式 _(リファレンス_) によって参照されるセルにリダイレクトされます。 SETATREF 関数を含むセルの数式はそのままです。
  
この  _set_expression_ 場合、UI またはオートメーションを使用して設定された値が参照セルに割り当てられます。それ以外の場合は、set_expression  _の内容_ が参照セルに割り当てられます。 これにより、参照セルに割り当てる前に、新しい値を変更または変換できます。 
  
SETATREF 関数には次の 2 つの関連する関数があります。 
  
- SETATREFEXPR 関数を使用すると、この関数を使用して、新しい値を _表set_expression。_ たとえば、SETATREFEXPR()-2 のset_expression、SETATREFEXPR()-2 in の値を使用します。  SETATREFEXPR の結果から 2 インチを減算するために使用できます。 
    
- SETATREFEVAL 関数を使用すると、一部のオブジェクトが評価され、結果  _set_expression_ 置き換えられる必要があります。 
    
SETATREF 関数は、図面ウィンドウのユーザー 操作で変更できるセルで使用するように設計されています。 次のセルがサポートされています。
  
- [Shape Transform] セクション - [Width]、[Height]、[Angle]、[PinX]、[PinY] の各セル
    
- [Text Transform] セクション - [TxtWidth]、[TxtHeight]、[TxtAngle]、[TxtPinX]、[TxtPinY] の各セル
    
- [1-D Endpoints] セクション - [BeginX]、[BeginY]、[EndX]、[EndY] の各セル
    
- [Controls] セクション - [Controls.X]、[Controls.Y] の各セル
    
- [Shape Data] セクション
    
SETATREF はセル値が変更される場所を変更しますので、イベントの発生に影響します。 セルに SETATREF が含まれている場合、SETATREF を含むセルではなく、SETATREF によって参照されるセルに対して **FormulaChanged** イベントと **CellChanged** イベントが発生します。 SETATREF を含むセルに SETATREFEXPR も含まれている場合は、関数パラメーターが変更されたため、SETATREF を含むセルに対して **FormulaChanged** イベントも発生します。 
  
SETATREF 関数についてのその他の重要な点は、以下のとおりです。
  
- SETATREF 関数は、他の SETATREF 関数に対し、最大 10 の参照を連鎖させることができます。 
    
- セルには、SETATREF 関数以外の式を含めることができます。1 つのセルに SETATREF を複数使用することもできます。
    
- 図形を接着している場合、Visio は同じシート内で連鎖している SETATREF 参照に従って、参照先のセルに接着する数式を配置します。 
    
- オートメーションは SETATREF 関数を認識して、参照先のセルの連鎖に従います。 
    
- GUARD 同様、SETATREF はシェイプシートの SETF 関数による変更からセルを保護しません。
    
## <a name="example1"></a>例 1

図形に [Width] というカスタム プロパティがあり、[Shape Transform] セクションの [Width] セルに次の数式が含まれているとします。
  
=SETATREF(Prop.Width)
  
ユーザーが UI で図形の幅を変更する場合、新しい値は [Prop.Width] セルに割り当てられます。ShapeTransform セクションの [Width] セルには割り当てられていない。[幅] セルの数式は変更されません。 図形データを使用して、図形の幅を設定することもできます。
  
## <a name="example2"></a>例 2

Visio ソリューションには階層関係を持つ図形が多く、親図形が移動する際には子図形も移動する必要があります。シェイプシートの SETATREF 関数を使用してこの関係を管理する例を次に示します。 
  
次の数式は子図形の [Shape Transform] セクションに含まれます。また、親図形からのオフセット寸法を追跡する [User.DeltaX] および [User.DeltaY] というユーザー セルを定義します。これにより、親図形が移動する際に子図形も移動することができます。また、子図形が移動する場合にも階層関係を保持することができます。
  
PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX
  
PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY
  
UI を使用して子図形を移動すると、SETATREFEXPR 関数のパラメーターとして新しい PinX 値と PinY 値が設定されます。 SETATREF 関数は、SETATREFEVAL で囲まれた数式を評価し、PinX と PinY を結果に置き換え、結果の数式は SETATREF 関数 User.DeltaX および User.DeltaY で参照されるユーザー セルに割り当てられます。 最後に、SETATREF (User.DeltaX または User.DeltaY) によって返される値が ParentShape のピン位置に追加され、子図形のピン位置が計算されます。
  

