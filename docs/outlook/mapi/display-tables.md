---
title: 表の表示
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c314ff6d-3e60-4b81-87ac-6ca6753ff633
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1b94b0ea69237be3675e1ea02fc3e2bfac337025
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406221"
---
# <a name="display-tables"></a>表の表示

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルでは、特定の種類のダイアログボックスを表示する方法について説明します。1つは、1つ以上のタブ付きプロパティページを表示し、1つ以上のプロパティを編集できます。 すべての表示テーブルに関連付けられているのは、 [imapiprop: IUnknown](imapipropiunknown.md)インターフェイスの実装です。 **imapiprop**の実装は、ダイアログボックスに表示されるプロパティデータを保持します。 
  
表示テーブル内の行は、ダイアログボックスに表示されるコントロールまたはユーザーインターフェイスオブジェクトを表します。 MAPI は、静的な値や、ユーザーが変更できる動的な値を持つ、さまざまな種類のコントロールを定義します。 ほとんどのコントロールは、 **imapiprop**の実装で管理されるプロパティに関連付けることができます。 ユーザーが変更可能なコントロールの値を変更すると、対応するプロパティが更新されます。 
  
サービスプロバイダーは、表示テーブルと**imapiprop**インターフェイスを実装します。 表示テーブルの作成は、スクリプト言語を使用してプログラムを記述するのと似ています。 サービスプロバイダーは、次の方法で表示テーブルを作成できます。 
  
- [builddisplaytable](builddisplaytable.md)関数を呼び出しています。 
    
    - や
    
- table データオブジェクトを使用して、表示テーブルに直接設定するカスタムコード ( [itabledata: IUnknown](itabledataiunknown.md)インターフェイスをサポートするオブジェクト) を含みます。 
    
**builddisplaytable**関数は、テーブルの表示構造からの情報をダイアログボックスリソースのビジュアル要素と組み合わせて、表示テーブルの行を作成します。 関数は、 [IMAPITable: IUnknown](imapitableiunknown.md)インターフェイスの実装へのポインターを返し、要求された場合は**itabledata**インターフェイスの実装へのポインターを返します。 
  
表示テーブルを作成するために**builddisplaytable**を使用することは簡単であり、表示が変更されたときに管理が容易になります。 ただし、 **builddisplaytable**を使用しないようにするサービスプロバイダーは、 **itabledata**のメソッドを使用するカスタムコードを使用して、表示テーブルを作成できます。 たとえば、プロパティページ用の既存のテンプレート構造を持つサービスプロバイダーは、 **builddisplaytable**を使用するのではなく、カスタムコードを作成する必要がある場合があります。
  
さまざまな方法で、サービスプロバイダーが表示テーブルのプロパティインターフェイスを実装できます。 これらには以下が含まれます。
  
- 標準[imapiprop: IUnknown](imapipropiunknown.md)実装を提供します。 
    
- 標準呼び出しを行う前に特別な処理を行う、ラップされた**imapiprop**の実装を提供します。 
    
- [ipropdata: imapiprop](ipropdataimapiprop.md)の実装を提供します。 
    
実装の種類は、表示されるデータの特性と責任のあるサービスプロバイダーによって異なります。 たとえば、2つのエディットコントロールのデータ間に暗黙的な関係があり、コントロールのいずれかが変更された場合、 **imapiprop**の実装では、他のコントロールの値を適切に変更する必要があります。 
  
表示テーブルには、必要な列に次のプロパティが設定されています。
  
|||
|:-----|:-----|
|**PR_XPOS**([PidTagXCoordinate](pidtagxcoordinate-canonical-property.md))  <br/> |**PR_YPOS**([PidTagYCoordinate](pidtagycoordinate-canonical-property.md))  <br/> |
|**PR_DELTAX**([PidTagDeltaX](pidtagdeltax-canonical-property.md))  <br/> |**PR_DELTAY**([PidTagDeltaY](pidtagdeltay-canonical-property.md))  <br/> |
|**PR_CONTROL_TYPE**([PidTagControlType](pidtagcontroltype-canonical-property.md))  <br/> |**PR_CONTROL_FLAGS**([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))  <br/> |
|**PR_CONTROL_STRUCTURE**([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))  <br/> |**PR_CONTROL_ID**([PidTagControlId](pidtagcontrolid-canonical-property.md))  <br/> |
   
 **PR_XPOS**および**PR_YPOS**コントロールの左上隅の X 座標と Y 座標を指定します。 水平方向の単位は、ダイアログベースの幅の単位の1/4 です。垂直の単位は、ダイアログベースの高さの単位の1/8 です。 現在のダイアログベースの単位は、現在のシステムフォントの高さと幅から計算されます。 座標は、プロパティページ領域の原点を基準にしています。 プロパティページのサイズは、約 200 (180 dialog unit) に制限されています。 
  
 **PR_DELTAX**および**PR_DELTAY**は、コントロールの幅と高さです。 これらは ULONG 値です。 幅の単位は、ダイアログベースの幅の単位の1/4 です。高さの単位は、ダイアログベースの高さの単位の1/8 です。 座標は、コントロールの原点を基準にします。 
  
他の4つのプロパティは、コントロールのさまざまな特性を示します。 **PR_CONTROL_TYPE**コントロールの種類を示します。 MAPI では、それぞれが異なる属性のセットを持つ12種類のコントロールが定義されています。 これらの属性については、flags プロパティ**PR_CONTROL_FLAGS**を参照してください。 属性の例としては、コントロールが編集可能かどうか、または必要かどうかが挙げられます。 
  
制御構造 ( **PR_CONTROL_STRUCTURE**) には、特定の種類のコントロールに関連する情報が含まれています。 それぞれの種類のコントロールについては、異なる構造で記述されています。 たとえば、編集コントロールは、 [DTBLEDIT](dtbledit.md)構造体で記述されます。 **DTBLEDIT**構造体には、コントロールに配置できる文字の数と特定の種類の文字、およびコントロールに表示されるプロパティを識別するプロパティタグをリストするメンバーが含まれています。 **PR_CONTROL_STRUCTURE**はバイナリプロパティとして格納されます。 
  
コントロール id **PR_CONTROL_ID**は、表示テーブルで記述されたダイアログボックス内のコントロールを一意に識別します。 **PR_CONTROL_ID**は、表示テーブルを作成するために**builddisplaytable**で使用される[DTCTL](dtctl.md)構造の*lpbNotif*および*cbNotif*メンバーに配置された値から設定されます。 MAPI は表示テーブルを結合する場合があるため、 **PR_CONTROL_ID**の識別子は常に一意である必要があります。 通常、プロバイダーは、一意性を保証するために[GUID](guid.md)構造を**PR_CONTROL_ID**に割り当てます。 **PR_CONTROL_ID**プロパティは、表示テーブル通知が生成されるときに、 [TABLE_NOTIFICATION](table_notification.md)構造に含まれています。 
  
表示テーブルの詳細については、「[表の実装](display-table-implementation.md)」および「display [table の通知につい](about-display-table-notifications.md)て」を参照してください。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

