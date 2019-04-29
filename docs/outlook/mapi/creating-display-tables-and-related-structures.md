---
title: 表示テーブルと関連する構造体の作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8548040-13ed-4a9f-a7ca-de610f94d7df
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 350272324c3827f4630f0cf35e3ade0ff213ac4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416245"
---
# <a name="creating-display-tables-and-related-structures"></a>表示テーブルと関連する構造体の作成
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルの作成は、スクリプト言語を使用してプログラムを記述するのと似ています。 表示テーブルを作成するには、 [builddisplaytable](builddisplaytable.md)を呼び出すか、カスタムコードを記述して、テーブルの行と列にデータを設定します。 一般に、 **builddisplaytable**手法はより単純なので、使用する必要があります。 
  
**builddisplaytable**を呼び出して MAPI に表示テーブルを作成するようにするには、まず構造の階層構造を構築する必要があります。 トップレベルの構造である[dtpage](dtpage.md)は、1つのタブ付きプロパティページを記述します。 **dtpage**のすべての構造体は、編集ボックスやオプションボタンなどの1つのコントロールを記述する[DTCTL](dtctl.md)構造体です。 各**DTCTL**構造体には、コントロールの種類に固有の構造が含まれています。 たとえば、 **DTCTL**構造体には、編集ボックスコントロールが記述されている場合、 **DTBLEDIT**構造体が含まれます。 オプションボタンの**DTCTL**構造体には、 **dtblradiobutton**構造体が含まれています。 
  
これらの構造は、直接**builddisplaytable**に関連しています。この関数のコンテキストの外部では意味がありません。 **builddisplaytable**を呼び出す場合は、1つ以上の**dtpage**構造を入力パラメーターとして渡します。 **dtpage**構造体には、 **DTCTL**構造体の配列と、配列内の**DTCTL**構造体の数のカウントが含まれています。 ダイアログボックスに表示するコントロールごとに1つの構造があります。 **dtpage**構造体にも、対応するヘルプファイルおよびダイアログボックスリソースの名前を表す文字列があります。 
  
**dtpage**構造の各**DTCTL**構造体には、コントロールのプロパティを設定するために使用される次のデータが含まれています。 
  
- **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) を設定するコントロールの種類を指定します。
    
- **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) を設定するための制御フラグ。
    
- **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) を設定するための通知データ。
    
- **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) を設定するためのコントロール構造。
    
**DTCTL**構造体にもリソース識別子が含まれています。また、エディットコントロールおよびコンボボックスコントロールの場合は、文字フィルターを使用します。 
  
**DTCTL**構造体の control 構造体メンバーは、コントロールの種類に固有のデータを記述します。 MAPI では、コントロールの種類ごとに異なる構造が定義されています。 たとえば、編集コントロールのデータは、 **DTBLEDIT**構造体で表されます。リストボックスのデータは、 **dtbllbx**構造体で表されます。 
  
次の図は、3種類の表示テーブル構造の関係を示しています。 この表示テーブルで説明されているダイアログボックスには、label および edit コントロールという2つのコントロールがあります。 **dtbllbx**構造体には、ラベルオフセットメンバがあります。これには、ラベルの文字列の開始位置を指定します。 通常、ラベル文字文字列は、構造体のすぐ後のメモリに配置されます。 
  
**表示テーブルの構造**
  
![テーブル構造を表示]する(media/dtstruct.gif "テーブル構造を表示")する
  
## <a name="see-also"></a>関連項目

- [表示テーブルの実装](display-table-implementation.md)

