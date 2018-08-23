---
title: 表示テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c314ff6d-3e60-4b81-87ac-6ca6753ff633
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 556d7551f64e075d1f15a945ddb1409c3b5a775f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799966"
---
# <a name="display-tables"></a>表示テーブル

  
  
**適用対象**: Outlook 
  
表示テーブルが特定の種類のダイアログ ボックスを表示する方法について説明などを表示して、おそらく 1 つまたは複数のプロパティを編集するのには専用の 1 つまたは複数のタブ付きプロパティ ページを持つ 1 つ。 関連付けられているテーブルは、すべてのディスプレイで、 [IMAPIProp: IUnknown](imapipropiunknown.md)インターフェイスの実装です。 **IMAPIProp**の実装では、ダイアログ ボックスに表示されるプロパティ データを保持します。 
  
ディスプレイ テーブル内の行は、コントロール、またはユーザー インターフェイス オブジェクト、ダイアログ ボックスに表示されているを表します。 MAPI では、静的な値を使用して一部使用し、ユーザーが変更される動的な値を使用して一部を使用する、コントロールの多くの種類を定義します。 ほとんどのコントロールは、 **IMAPIProp**の実装と管理プロパティに関連付けることができます。 ユーザーは、変更可能なコントロールの値を変更するときは、対応するプロパティが更新されます。 
  
サービス プロバイダーは、テーブルの表示と**IMAPIProp**インターフェイスを実装します。 表示テーブルを作成することは、スクリプト言語でプログラムを記述に似ています。 サービス プロバイダーは、表示のテーブルを作成できます。 
  
- [BuildDisplayTable](builddisplaytable.md)関数を呼び出しています。 
    
    - または、
    
- 直接オブジェクトを使用して、テーブル データの表示テーブルを設定するカスタム コードを含む-をサポートするオブジェクトの[ITableData: IUnknown](itabledataiunknown.md)インタ フェースです。 
    
**BuildDisplayTable**関数は、テーブルの行の表示を作成するダイアログ ボックスのリソースからの視覚的要素を持つディスプレイ テーブルの構造体から情報を組み合わせたものです。 関数へのポインターを返します。、 [IMAPITable: IUnknown](imapitableiunknown.md)インターフェイスの実装、および、要求された場合、 **ITableData**インターフェイスの実装へのポインター。 
  
**BuildDisplayTable**を使用して、表示された表を作成するのには単純で、ディスプレイの視覚的な要素を変更するときは、保守を容易です。 ただし、 **BuildDisplayTable**を使用しないようにするサービス プロバイダーは、 **ITableData**のメソッドを使用するカスタム コードで表示テーブルを作成できます。 などのサービス プロバイダーのプロパティ ページの既存のテンプレートの構造であることをすることも**BuildDisplayTable**を使用するのではなく、カスタム コードを作成します。
  
さまざまなサービス ・ プロバイダーは、表示された表のプロパティ インターフェイスを実装する方法があります。 これらは次のとおりです。
  
- 標準を提供する[IMAPIProp: IUnknown](imapipropiunknown.md)実装します。 
    
- 標準的な呼び出しを行う前に特別な処理を含むラップされた**IMAPIProp**実装を提供します。 
    
- 提供する、 [IPropData: IMAPIProp](ipropdataimapiprop.md)の実装です。 
    
実装の種類は、表示するデータの特性と、担当のサービス プロバイダーによって異なります。 などの 2 つのエディット コントロール内のデータの間で暗黙のリレーションシップがあるし、コントロールのいずれかが変更された、 **IMAPIProp**実装する必要があります、他のコントロールの値を適切に変更します。 
  
表示テーブルでは、必要な列セットは次のプロパティがあります。
  
|||
|:-----|:-----|
|**PR_XPOS**([PidTagXCoordinate](pidtagxcoordinate-canonical-property.md))  <br/> |**PR_YPOS**([PidTagYCoordinate](pidtagycoordinate-canonical-property.md))  <br/> |
|**PR_DELTAX**([PidTagDeltaX](pidtagdeltax-canonical-property.md))  <br/> |**PR_DELTAY**([PidTagDeltaY](pidtagdeltay-canonical-property.md))  <br/> |
|**PR_CONTROL_TYPE**([PidTagControlType](pidtagcontroltype-canonical-property.md))  <br/> |**PR_CONTROL_FLAGS**([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))  <br/> |
|**PR_CONTROL_STRUCTURE**([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))  <br/> |**PR_CONTROL_ID**([PidTagControlId](pidtagcontrolid-canonical-property.md))  <br/> |
   
 **PR_XPOS**と**PR_YPOS**は、コントロールの左上隅の X と Y 座標を指定します。 水平方向の単位は、1/4、ダイアログ ベース単位の幅です。垂直方向の単位は、ダイアログ ベースの高さの単位の 1/8 です。 Windows では、現在のダイアログの基本単位から現在のシステム フォントの幅と高さを計算します。 座標は、プロパティ ページ領域の原点を基準にしています。 プロパティ ページのサイズは、ダイアログ単位を約 180 から 200 に制限されます。 
  
 **PR_DELTAX**と**PR_DELTAY**は、幅と、コントロールの高さです。 これらは、ULONG 値です。 幅の単位は、1/4、ダイアログ ベース単位の幅です。高さの単位は、ダイアログ ベースの高さの単位の 1/8 です。 座標は、コントロールの原点に対する相対座標です。 
  
他の 4 つのプロパティは、コントロールのさまざまな特性について説明します。 **PR_CONTROL_TYPE**は、コントロールの種類を示します。 MAPI では、12 種類のそれぞれ異なる一連の属性を持つコントロールを定義します。 フラグは、 **PR_CONTROL_FLAGS**では、これらの属性が記載されています。 属性の例には、コントロールは、編集可能または必要であるかどうかが含まれます。 
  
制御構造体、 **PR_CONTROL_STRUCTURE**には、コントロールの特定の種類に関連する情報が含まれています。 異なる構造を持つコントロールの種類を説明します。 などのエディット コントロールは、そのような[DTBLEDIT](dtbledit.md)構造を説明します。 **DTBLEDIT**構造体には、メンバーには数と、使用できるコントロールとプロパティを識別するプロパティ タグの値を持つ文字の特定の種類は、コントロールに表示するリストが含まれています。 **PR_CONTROL_STRUCTURE**は、バイナリ プロパティとして格納されます。 
  
コントロール id、 **PR_CONTROL_ID**は、表示された表で説明されているダイアログ ボックスでコントロールを一意に識別します。 **PR_CONTROL_ID**は、表示された表を作成するのには**BuildDisplayTable**で使用される[DTCTL](dtctl.md)構造体の*lpbNotif*と*cbNotif*のメンバーに値を設定します。 MAPI は、場合によって表示のテーブルを結合ため、 **PR_CONTROL_ID**内の識別子は常に一意であります。 通常、プロバイダーは、その一意性を保証する**PR_CONTROL_ID**する[GUID](guid.md)構造体を割り当てます。 表示テーブルの通知が生成されるときは、 [TABLE_NOTIFICATION](table_notification.md)構造体の**PR_CONTROL_ID**プロパティが含まれます。 
  
詳細表示のテーブルは、[テーブルの実装の表示](display-table-implementation.md)と[詳細表示のテーブルの通知](about-display-table-notifications.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

