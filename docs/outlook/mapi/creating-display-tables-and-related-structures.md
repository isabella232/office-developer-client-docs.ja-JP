---
title: 表示テーブルと関連する構造体の作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a8548040-13ed-4a9f-a7ca-de610f94d7df
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 853a8db028d0e902f785cc3198e7994404af3ef1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592677"
---
# <a name="creating-display-tables-and-related-structures"></a>表示テーブルと関連する構造体の作成
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルの作成は、スクリプト言語を使用したプログラムの作成に似ています。 表示テーブルを作成するには [、BuildDisplayTable](builddisplaytable.md) を呼び出すか、カスタム コードを記述してテーブルの行と列を設定します。 一般に **、BuildDisplayTable** の手法は、より簡単なので使用する必要があります。 
  
**BuildDisplayTable** を呼び出して MAPI に表示テーブルの作成を求める前に、構築する必要がある構造の階層があります。 トップ レベルの構造 [DTPAGE は](dtpage.md)、単一のタブ付きプロパティ ページを表します。 すべての **DTPAGE 構造** では、編集ボックスやオプション ボタンなど、1 つのコントロールを記述する [DTCTL](dtctl.md) 構造です。 各 **DTCTL** 構造には、コントロールの種類に固有の構造が含まれる。 たとえば **、DTCTL 構造体に編集** ボックス コントロールが記述されている場合 **、DTBLEDIT 構造が含まれるとします** 。 オプション **ボタンの DTCTL** 構造には **、DTBLRADIOBUTTON 構造が含** まれる。 
  
これらの構造体は **、BuildDisplayTable に直接関連しています**。この関数のコンテキストの外側には意味はありません。 **BuildDisplayTable を呼び出す場合** は、1 つ以上の **DTPAGE** 構造体を入力パラメーターとして渡します。 **DTPAGE 構造体には****、DTCTL** 構造体の配列と、配列内の **DTCTL** 構造体の数が含まれています。 ダイアログ ボックスに表示するコントロールごとに 1 つの構造があります。 **DTPAGE** 構造体には、対応するヘルプ ファイルとダイアログ ボックス リソースの名前を表す文字列も含まれています。 
  
DTPAGE **構造体内** の **各 DTCTL** 構造には、コントロールのプロパティを設定するために使用される次のデータが含まれます。 
  
- コントロールの種類 ([PidTagControlType](pidtagcontroltype-canonical-property.md) **)** PR_CONTROL_TYPE設定するコントロールの種類です。
    
- [(PidTagControlFlags)](pidtagcontrolflags-canonical-property.md)PR_CONTROL_FLAGS設定のコントロール フラグ。 
    
- 設定の通知データ [(PidTagControlId](pidtagcontrolid-canonical-property.md) **PR_CONTROL_ID)**
    
- プロパティ ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) を **PR_CONTROL_STRUCTURE** コントロール構造。
    
**DTCTL 構造体** には、リソース識別子と、編集およびコンボ ボックス コントロールの文字フィルターも含まれます。 
  
**DTCTL** 構造体のコントロール構造メンバーは、コントロールの種類に固有のデータを記述します。 MAPI は、コントロールの種類ごとに異なる構造を定義します。 たとえば、編集コントロールのデータは **DTBLEDIT 構造で表** されます。リスト ボックスのデータは **DTBLLBX 構造で表** されます。 
  
次の図に、3 種類の表示テーブル構造の関係を示します。 この表示テーブルで説明するダイアログ ボックスには、ラベルと編集コントロールの 2 つのコントロールがあります。 **DTBLLBX** 構造体には、ラベルの文字列の開始位置を示す、いくつかのコントロール構造と同様に、ラベル オフセット メンバーがあります。 ラベル文字列は、通常、構造体の直後にメモリに配置されます。 
  
**表示テーブルの構造**
  
![表示テーブルの構造](media/dtstruct.gif "表示テーブルの構造")
  
## <a name="see-also"></a>関連項目

- [表示テーブルの実装](display-table-implementation.md)

