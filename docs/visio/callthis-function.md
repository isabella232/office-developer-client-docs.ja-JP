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
description: Microsoft Visual Basic for Applications (VBA) プロジェクトでプロシージャを呼び出します。
ms.openlocfilehash: 7e0f0bafa39d6c1eb1fd39535506981c937ce8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413816"
---
# <a name="callthis-function"></a>CALLTHIS 関数

Microsoft Visual Basic for Applications (VBA) プロジェクトでプロシージャを呼び出します。
  
## <a name="syntax"></a>構文

CALLTHIS(" ** *procedure* ** ",[" ** *project* ** "],[ ** *arg1* **, ** *arg2* **,...]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _procedure_ <br/> |必須  <br/> |**String** <br/> | 呼び出すプロシージャの名前を指定します。  <br/> |
| _project_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |プロシージャが含まれるプロジェクトを指定します。  <br/> |
| _arg_ <br/> |省略可能  <br/> |**数値型 (Number)、文字列型 (String)、日付型 (Date)、または通貨型 (Currency)** <br/> |パラメーターとしてプロシージャに渡されます。  <br/> |
   
## <a name="remarks"></a>注釈

VBA プロジェクトでは、  *プロシージャは次*  のように定義されます。 
  
procedure(*vsoShape* As Visio。Shape [arg1 As type, arg2 As type...]) 
  
*ここで、vsoShape* は、評価される **CALLTHIS** 数式と _arg1 、arg2_..を含む Shape オブジェクトへの参照です。は、その数式で指定された引数です。 
  
*vsoShape は*、C++ メンバー プロシージャに渡される "this" 引数と非常に似たものに注意してください。したがって、名前 "CALLTHIS." 実際には、CALLTHIS を含む数式を含むセルは、「このプロシージャを呼び出して、自分の図形への参照を渡す」と読み取ります。 
  
project _が_ 指定されている場合、Microsoft Visio開いているすべてのドキュメントがスキャンされ、そのプロジェクトに含まれるプロジェクトの _プロシージャが呼_ び出されます。 project _が_ 省略されている場合、または null ("") の場合、Visio は、評価される CALLTHIS 数式を含むドキュメントの VBA プロジェクトにあると仮定します。 
  
_arg1 、_ _arg2..._ の数値は、外部単位で渡されます。 たとえば、高さが 3 cm の図形から [Height] セルの値を渡すと、3 が渡されます。 数値を別の単位に変換して渡すには、FORMATEX 関数を使用するか、NULL 値と単位の組み合わせを追加して明示的に単位を適用します (0 ft + Height など)。 
  
CALLTHIS 関数の 2 番目のカンマはオプションです。 これは、プロシージャに追加するパラメーターの数に応じて指定します。 2 番目のコンマを追加しない以外のパラメーターを使用しない場合は  `(vsoShape as Visio.Shape)` 、CALLTHIS("",) を使用します。 たとえばパラメーターを 2 つ追加する場合は、CALLTHIS("",,,) のように記述します。 
  
CALLTHIS 関数は常に 0 に評価され、プロシージャの呼び出しは再計算プロセスが終了した後、アイドル時間中に行われます。  _プロシージャ_ は値を返しますが、Visio無視します。  _プロシージャ_ は、Visio が文書内の別のセルの数式または結果を設定することで認識できる値を返しますが、CALLTHIS数式を上書きしない限り、プロシージャを呼び出したセルは返されません。
  
CALLTHIS 関数では、図面のプロジェクトが別のプロジェクトを参照していなくても、そのプロジェクトを呼び出すことができます。この点が、RUNADDON 関数とは異なる点です。 
  
> [!NOTE]
>  Visio インスタンスが数式の CALLTHIS 関数を評価する場合、その結果呼び出された VBA コードでは、この数式を使用しているセルを含んだ図面を閉じないでください。アプリケーション エラーが発生して Visio が終了します。 
  
CALLTHIS 関数を使用するセルを含んだ図面を閉じる必要がある場合、次のいずれかの操作を行います。 
  
- VBA 以外のコードを使用して図面を閉じます。
    
- 閉じる図面以外のプロジェクトから図面を閉じます。
    
- 図面を閉じる代わりに、ウィンドウを閉じるためのウィンドウ メッセージを図面に通知します。
    
Visio のコードの実行に関する詳細については、この『シェイプシート リファレンス』の「[Visio のセキュリティ設定およびコードの実行について](about-security-settings-and-running-code-in-visio-shapesheet.md)」を参照してください。 
  
## <a name="example-1"></a>例 1

CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))
  
モジュール内の p という名前のプロシージャを呼び出し、Height の値をセンチメートル単位 (7.62 cm など) で渡します。
  
## <a name="example-2"></a>例 2

CALLTHIS("q",,0 cm+Height,Width)
  
モジュール内の q という名前のプロシージャを呼び出し、セルの高さをセンチメートル単位で、幅を内部単位で渡します。
  
## <a name="example-3"></a>例 3

ThisDocument クラス モジュールの  *次の手順を*  使用します。 
  
図形の [EventDblClick] セルでは、上記のプロシージャと共に次のいずれかの構文を使用します。
  
CALLTHIS("ThisDocument.A",)
  
CALLTHIS("ThisDocument.B","Click")
  
CALLTHIS("ThisDocument.C",,"Click", " OK.")
  

