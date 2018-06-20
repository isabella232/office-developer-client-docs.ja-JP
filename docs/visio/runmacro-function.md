---
title: RUNMACRO 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033809
localization_priority: Normal
ms.assetid: 86b0f071-5e0b-56de-ff5b-63c114ad823a
description: マクロを Microsoft Visual Basic for Applications (VBA) プロジェクトします。
ms.openlocfilehash: e3dd989956ce9c5f795ae3ef0d8535ab2776d6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806340"
---
# <a name="runmacro-function"></a>RUNMACRO 関数

マクロを Microsoft Visual Basic for Applications (VBA) プロジェクトします。 
  
## <a name="syntax"></a>構文

RUNMACRO (* **マクロ名** * [、* * *projname_opt* * *]) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _マクロ名_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |呼び出すマクロの名前を指定します。  <br/> |
| _projname_opt_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> | マクロが含まれるプロジェクトを指定します。  <br/> |
   
## <a name="remarks"></a>注釈

プロジェクトが指定されている場合、Microsoft Visio は、1 つ含まれている_projname_opt_と呼び出し_マクロ名_をプロジェクト内のすべての開いているドキュメントをスキャンします。 _Projname_opt_が省略されるか null の場合 ("")、_マクロ名_を評価する RUNMACRO 数式を含む文書の VBA プロジェクト内にあると見なされます。 
  
RUNMACRO 関数は、_マクロ名_に評価される式を所有している図形への参照に合格しないことで、CALLTHIS 関数とは異なります。 CALLTHIS のような RUNMACRO 関数は_projname_opt_をそれへの呼び出しをへの参照を必要としません。 
  
 Visio インスタンスが数式の RUNMACRO 関数を評価するときに呼び出す VBA コードでは、この数式を使用しているセルを含んだ図面を閉じないでください。アプリケーション エラーが発生して Visio が終了します。 
  
RUNMACRO 関数を使用するセルを含んだ図面を閉じる必要がある場合、次のいずれかの操作を行います。
  
- VBA 以外のコードを使用して図面を閉じます。
    
- 閉じる図面以外のプロジェクトから図面を閉じます。
    
- 図面を閉じる代わりに、ウィンドウを閉じるためのウィンドウ メッセージを図面に通知します。
    
Visio のコードの実行の詳細については、[セキュリティ設定、および Visio のコードの実行について](about-security-settings-and-running-code-in-visio-shapesheet.md)のこの「シェイプ シート リファレンスを参照してください。 
  
## <a name="example"></a>例

次の例では、RUNMACRO 数式を含む VBA プロジェクトの ThisDocument クラス モジュールの MyTest というマクロを呼び出します。 
  
RUNMACRO ("ThisDocument.MyTest") 
  

