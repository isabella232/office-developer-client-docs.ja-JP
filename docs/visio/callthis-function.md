---
title: CALLTHIS 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251403
localization_priority: Normal
ms.assetid: 461abfc1-d2cc-2354-1c2f-395c9e351a78
description: (VBA) プロジェクトを Microsoft Visual Basic for Applications プロシージャを呼び出します。
ms.openlocfilehash: 04065384453e55b745daa89273fb4c23b32fb90c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804940"
---
# <a name="callthis-function"></a>CALLTHIS 関数

(VBA) プロジェクトを Microsoft Visual Basic for Applications プロシージャを呼び出します。
  
## <a name="syntax"></a>構文

CALLTHIS ("* **手順** *」、["* **プロジェクト** *」]、[* * *arg1* * *、* **引数 2* * *,...]) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _手順_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 呼び出すプロシージャの名前を指定します。  <br/> |
| _プロジェクト_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |プロシージャが含まれるプロジェクトを指定します。  <br/> |
| _arg_ <br/> |省略可能  <br/> |**数値、文字列、日付、または通貨** <br/> |パラメーターとしてプロシージャに渡されます。  <br/> |
   
## <a name="remarks"></a>注釈

VBA プロジェクトでは、*プロシージャ*は次のように定義されます。 
  
プロシージャ (*vsoShape*としてほとんどの場合において [arg1 と arg2... の種類として、入力]) 
  
*vsoShape*への参照が評価される CALLTHIS 数式を含んだ**Shape**オブジェクトおよび_arg1_、 *arg2*がその数式で指定された引数。 
  
その*vsoShape*は、C++ のメンバー プロシージャに渡される"this"引数と同じように非常に近いものに注意してください。したがって名前"CALLTHIS"にします。 実際には、CALLTHIS を含む数式を含むセル読み取ることができるようには、「このプロシージャ呼び出すし、、図形に対する参照を渡すこと。 
  
_プロジェクト_が指定されている場合、Microsoft Visio は、1 つ含まれている_プロジェクト_と呼び出し_プロシージャ_そのプロジェクト内のすべての開いているドキュメントをスキャンします。 _プロジェクト_が省略されるか null の場合 ("")、Visio では、対象となる CALLTHIS 数式を含む文書の VBA プロジェクト内の_プロシージャ_が前提としています。 
  
_Arg1_に数値、 _arg2..._ は外部単位で渡されます。 たとえば、高さが 3 cm の図形から [Height] セルの値を渡すと、3 が渡されます。 渡すには別の単位数が、FORMATEX 関数を使用または明示的に null 単位 1 組、0 ft + 高さなどを追加することで単位を変換します。 
  
CALLTHIS 関数の 2 番目のカンマはオプションです。 それは、プロシージャに追加する追加のパラメーターの数に対応しています。 以外の場合は、追加パラメーターを使用しないと、 `(vsoShape as Visio.Shape)` 、2 つ目のコンマを追加しません。CALLTHIS("",) を使用します。 2 つのパラメーターを追加する場合は、たとえば、CALLTHIS("",,,) を使用します。 
  
CALLTHIS 関数は常に 0 に評価し、_プロシージャ_への呼び出しは、再計算処理が完了したら、アイドル時間中に発生します。  _プロシージャ_は、値を返すことができますが、Visio では無視されます。  _プロシージャ_では、CALLTHIS 数式を上書きする場合を除き、Visio は、ドキュメント内の数式または他のセルの結果を設定することで認識できる値がない_プロシージャ_を呼び出したセルを返します。
  
CALLTHIS 関数では、図面のプロジェクトが別のプロジェクトを参照していなくても、そのプロジェクトを呼び出すことができます。この点が、RUNADDON 関数とは異なる点です。 
  
> [!NOTE]
>  Visio インスタンスが数式の CALLTHIS 関数を評価する場合、その結果呼び出された VBA コードでは、この数式を使用しているセルを含んだ図面を閉じないでください。アプリケーション エラーが発生して Visio が終了します。 
  
CALLTHIS 関数を使用するセルを含んだ図面を閉じる必要がある場合、次のいずれかの操作を行います。 
  
- VBA 以外のコードを使用して図面を閉じます。
    
- 閉じる図面以外のプロジェクトから図面を閉じます。
    
- 図面を閉じる代わりに、ウィンドウを閉じるためのウィンドウ メッセージを図面に通知します。
    
Visio のコードの実行の詳細について[セキュリティ設定について、Visio でのコードの実行](about-security-settings-and-running-code-in-visio-shapesheet.md)でこの「シェイプ シート リファレンスを参照してください。 
  
## <a name="example-1"></a>例 1

CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))
  
モジュール内の p という名前のプロシージャを呼び出し、Height の値をセンチメートル単位 (7.62 cm など) で渡します。
  
## <a name="example-2"></a>例 2

CALLTHIS("q",,0 cm+Height,Width)
  
モジュール内の q という名前のプロシージャを呼び出し、セルの高さをセンチメートル単位で、幅を内部単位で渡します。
  
## <a name="example-3"></a>例 3

*ThisDocument*クラス モジュールに次の手順を使用します。 
  
図形の [EventDblClick] セルでは、上記のプロシージャと共に次のいずれかの構文を使用します。
  
CALLTHIS("ThisDocument.A",)
  
CALLTHIS("ThisDocument.B",,"Click")
  
CALLTHIS("ThisDocument.C",,"Click", " OK.")
  

