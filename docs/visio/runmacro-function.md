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
description: Microsoft Visual Basic for Applications (VBA) プロジェクトでマクロを呼び出します。
ms.openlocfilehash: 77045bd67fe9be9aab14e73199b33b93c6d70c2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428089"
---
# <a name="runmacro-function"></a>RUNMACRO 関数

Microsoft Visual Basic for Applications (VBA) プロジェクトでマクロを呼び出します。 
  
## <a name="syntax"></a>構文

RUNMACRO (** *macroname* ** [, **** projname_opt ** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _macroname_ <br/> |必須  <br/> |**String** <br/> |呼び出すマクロの名前を指定します。  <br/> |
| _projname_opt_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> | マクロが含まれるプロジェクトを指定します。  <br/> |
   
## <a name="remarks"></a>注釈

プロジェクトが指定されている場合、Microsoft Visioが開いているすべてのドキュメントをスキャンして、そのプロジェクトのマクロprojname_opt呼び出します。 この _projname_opt_ または null ("") の場合、マクロ名は、評価される RUNMACRO 数式を含むドキュメントの VBA プロジェクトにあると見なされます。 
  
RUNMACRO 関数は、マクロ名に対して評価される数式を所有する図形への参照を渡すという点で CALLTHIS 関数とは  _異なります_。 CALLTHIS と同様に、RUNMACRO 関数は、呼び出しを行う  _projname_opt参照を_ 必要としません。 
  
 Visio インスタンスが数式の RUNMACRO 関数を評価するときに呼び出す VBA コードでは、この数式を使用しているセルを含んだ図面を閉じないでください。アプリケーション エラーが発生して Visio が終了します。 
  
RUNMACRO 関数を使用するセルを含んだ図面を閉じる必要がある場合、次のいずれかの操作を行います。
  
- VBA 以外のコードを使用して図面を閉じます。
    
- 閉じる図面以外のプロジェクトから図面を閉じます。
    
- 図面を閉じる代わりに、ウィンドウを閉じるためのウィンドウ メッセージを図面に通知します。
    
Visio でのコードの実行に関する詳細については、この『シェイプシート リファレンス』の「[Visio のセキュリティ設定およびコードの実行について](about-security-settings-and-running-code-in-visio-shapesheet.md)」を参照してください。 
  
## <a name="example"></a>例

次の例では、RUNMACRO 数式を含む VBA プロジェクトの ThisDocument クラス モジュールの MyTest というマクロを呼び出します。 
  
RUNMACRO ("ThisDocument.MyTest") 
  

