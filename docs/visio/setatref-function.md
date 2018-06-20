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
description: リダイレクトは、別のセルに、ユーザー インターフェイス (UI) またはオートメーションでのアクションの結果の値を更新します。
ms.openlocfilehash: 69a9cb93ae3fbd807ef4f306be386f5389a6cfeb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806371"
---
# <a name="setatref-function"></a>SETATREF 関数

リダイレクトは、別のセルに、ユーザー インターフェイス (UI) またはオートメーションでのアクションの結果の値を更新します。 
  
## <a name="syntax"></a>構文

SETATREF (* **参照** * [、* **式** * [、* * *ignore_eval* * *]) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _reference_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |更新された値をリダイレクトするセルに対する参照を指定します。  <br/> |
| _セット式_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |_参照_に割り当てられている式を指定します。  <br/> |
| _ignore_eval_ <br/> |省略可能  <br/> |**ブール型 (Boolean)** <br/> |SETATREF 関数の評価 (0) に TRUE の場合、ゼロです。FALSE の場合 (既定値) SETATREF 関数評価_の参照_の値にします。  <br/> |
   
## <a name="remarks"></a>備考

SETATREF 数式を含むセルを更新するための Microsoft Visio 図面ウィンドウ、またはオートメーション メソッドでは、ユーザーの操作が発生した場合と、値は SETATREF 数式 (_参照_) で参照されているセルへ代わりにリダイレクトされます。 SETATREF 関数を含むセルの数式はそのままの状態のままになります。
  
_セット式_を省略した場合、UI またはオートメーションを使用して設定値は参照先のセルにそれ以外の場合、_式_の内容は、参照先のセルに割り当てられます。 これにより、新しい値を変更または参照先のセルに割り当てられる前に変換します。 
  
SETATREF 関数には次の 2 つの関連する関数があります。 
  
- SETATREFEXPR 関数を_式_内で新しい値を表すことを使用することができます。 など、_セット式_が SETATREFEXPR ()-2 にします。 SETATREFEXPR の結果から 2 インチの減算に使用できます。 
    
- SETATREFEVAL 関数、_式_の一部を評価してその結果で置き換えられますことを示すために使用することができます。 
    
SETATREF 関数は図面ウィンドウのユーザー アクションによって変更可能なセルで使用するために設計されています。 次のセルがサポートされています。
  
- [Shape Transform] セクション - [Width]、[Height]、[Angle]、[PinX]、[PinY] の各セル
    
- [Text Transform] セクション - [TxtWidth]、[TxtHeight]、[TxtAngle]、[TxtPinX]、[TxtPinY] の各セル
    
- [1-D Endpoints] セクション - [BeginX]、[BeginY]、[EndX]、[EndY] の各セル
    
- [Controls] セクション - [Controls.X]、[Controls.Y] の各セル
    
- [Shape Data] セクション
    
SETATREF はセルの値の変更の場所を変更、イベントの発生に影響を与えます。 セルが SETATREF を含む場合は、SETATREF を含むセルではない、SETATREF が参照するセルに、 **FormulaChanged**イベントおよび**CellChanged**イベントが発生します。 SETATREF を含むセルが SETATREFEXPR に含まれる場合、関数のパラメーターが変更されるため、SETATREF を含むセルに対しても**FormulaChanged**イベントが発生します。 
  
SETATREF 関数についてのその他の重要な点は、以下のとおりです。
  
- SETATREF 関数は、他の SETATREF 関数に対し、最大 10 の参照を連鎖させることができます。 
    
- セルには、SETATREF 関数以外の式を含めることができます。1 つのセルに SETATREF を複数使用することもできます。
    
- 図形を接着している場合、Visio は同じシート内で連鎖している SETATREF 参照に従って、参照先のセルに接着する数式を配置します。 
    
- オートメーションは SETATREF 関数を認識して、参照先のセルの連鎖に従います。 
    
- GUARD 同様、SETATREF はシェイプシートの SETF 関数による変更からセルを保護しません。
    
## <a name="example1"></a>Example1

図形に [Width] というカスタム プロパティがあり、[Shape Transform] セクションの [Width] セルに次の数式が含まれているとします。
  
=SETATREF(Prop.Width)
  
Prop.Width [ShapeTransform] セクションでは、[Width] セルにセルに新しい値が割り当てられているユーザーが UI で図形の幅を変更する場合、幅のセルの数式は変更されません。 図形データを使用して図形の幅を設定することもできます。
  
## <a name="example2"></a>Example2

Visio ソリューションには階層関係を持つ図形が多く、親図形が移動する際には子図形も移動する必要があります。シェイプシートの SETATREF 関数を使用してこの関係を管理する例を次に示します。 
  
次の数式は子図形の [Shape Transform] セクションに含まれます。また、親図形からのオフセット寸法を追跡する [User.DeltaX] および [User.DeltaY] というユーザー セルを定義します。これにより、親図形が移動する際に子図形も移動することができます。また、子図形が移動する場合にも階層関係を保持することができます。
  
PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX
  
PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY
  
UI を使用して、子の図形を移動すると、SETATREFEXPR 関数のパラメーターとして新しい PinX と PinY の値が設定されます。 SETATREF 関数は SETATREFEVAL で囲まれた式を評価し、[pinx] と [piny]、その結果に置き換えます、SETATREF function—User.DeltaX と User.DeltaY で参照されているユーザーのセルに式を割り当てられます。 最後に、SETATREF User.DeltaX (User.DeltaY) によって返される値は、子図形の pin の位置を計算する ParentShape の暗証番号 (pin) の場所に追加されます。
  

