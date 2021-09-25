---
title: テーブルの表示
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c314ff6d-3e60-4b81-87ac-6ca6753ff633
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fa65f150639a0604ee84f038c92cec0b0a10e43e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588173"
---
# <a name="display-tables"></a>テーブルの表示

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルは、特定の種類のダイアログ ボックス (1 つ以上のタブ付きプロパティ ページを含む) を表示し、1 つ以上のプロパティを編集する方法について説明します。 すべての表示テーブルに関連付けられている [のは、IMAPIProp : IUnknown インターフェイスの](imapipropiunknown.md) 実装です。 **IMAPIProp の** 実装では、ダイアログ ボックスに表示されるプロパティ データが保持されます。 
  
表示テーブルの行は、ダイアログ ボックスに表示されるコントロールまたはユーザー インターフェイス オブジェクトを表します。 MAPI は、静的な値を持つコントロールと、ユーザーが変更できる動的な値を持つコントロールの多くの種類を定義します。 ほとんどのコントロールは、IMAPIProp 実装で管理されている **プロパティに関連付** けできます。 ユーザーが変更可能なコントロールの値を変更すると、対応するプロパティが更新されます。 
  
サービス プロバイダーは、表示テーブルと **IMAPIProp インターフェイスを実装** します。 表示テーブルの作成は、スクリプト言語を使用したプログラムの作成に似ています。 サービス プロバイダーは、次の方法で表示テーブルを作成できます。 
  
- [BuildDisplayTable 関数を呼び出](builddisplaytable.md)します。 
    
    - Or -
    
- テーブル データ オブジェクト [(ITableData : IUnknown](itabledataiunknown.md) インターフェイスをサポートするオブジェクト) を使用して表示テーブルに直接設定するカスタム コードを含む。 
    
**BuildDisplayTable 関数は**、表示テーブル構造の情報とダイアログ ボックス リソースの視覚的要素を組み合わせ、表示テーブルの行を作成します。 この関数は [、IMAPITable : IUnknown](imapitableiunknown.md) インターフェイス実装へのポインターと、要求された場合は **ITableData** インターフェイス実装へのポインターを返します。 
  
**BuildDisplayTable を使用** して表示テーブルを作成する方法は簡単で、表示の視覚的要素が変化するとメンテナンスが容易になります。 ただし **、BuildDisplayTable** を使用しないサービス プロバイダーは **、ITableData** のメソッドを使用するカスタム コードを使用して表示テーブルを作成できます。 たとえば、プロパティ ページに既存のテンプレート構造を持つサービス プロバイダーは **、BuildDisplayTable** を使用するのではなく、カスタム コードを作成する必要があります。
  
サービス プロバイダーが表示テーブルのプロパティ インターフェイスを実装するには、さまざまな方法があります。 たとえば、次の環境です。:
  
- 標準の [IMAPIProp : IUnknown 実装を指定](imapipropiunknown.md) します。 
    
- 標準呼び出しを行う前に、特別な処理を含むラップされた **IMAPIProp** 実装を提供します。 
    
- [IPropData : IMAPIProp 実装を指定](ipropdataimapiprop.md)します。 
    
実装の種類は、表示するデータの特性と責任あるサービス プロバイダーによって異なります。 たとえば、2 つの編集コントロール内のデータの間に暗黙的な関係が生じ、1 つのコントロールが変更される場合 **、IMAPIProp** 実装は他のコントロールの値を適切に変更する必要があります。 
  
表示テーブルには、必要な列セットに次のプロパティがあります。
  
|||
|:-----|:-----|
|**PR_XPOS** ([PidTagXCoordinate](pidtagxcoordinate-canonical-property.md))  <br/> |**PR_YPOS** ([PidTagYCoordinate](pidtagycoordinate-canonical-property.md))  <br/> |
|**PR_DELTAX** ([PidTagDeltaX](pidtagdeltax-canonical-property.md))  <br/> |**PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md))  <br/> |
|**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md))  <br/> |**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))  <br/> |
|**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))  <br/> |**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))  <br/> |
   
 **PR_XPOS** および **PR_YPOS** コントロールの左上隅の X 座標と Y 座標を指定します。 水平方向の単位は、ダイアログの基本幅単位の 1/4 です。垂直方向の単位は、ダイアログベースの高さ単位の 1/8 です。 Windowsは、現在のシステム フォントの高さと幅から現在のダイアログの基本単位を計算します。 座標は、プロパティ ページ領域の原点を基準にしています。 プロパティ ページのサイズは、ダイアログ 単位で約 200 ~ 180 個に制限されます。 
  
 **PR_DELTAX** と **PR_DELTAY** は、コントロールの幅と高さです。 これらは ULONG 値です。 幅の単位は、ダイアログの基本幅単位の 1/4 です。高さの単位は、ダイアログベースの高さ単位の 1/8 です。 座標は、コントロールの原点を基準にしています。 
  
他の 4 つのプロパティでは、コントロールのさまざまな特性について説明します。 **PR_CONTROL_TYPE** コントロールの種類を示します。 MAPI では、12 種類のコントロールが定義されます。それぞれ異なる属性のセットを持っています。 これらの属性については、flags プロパティ **、PR_CONTROL_FLAGS。** 属性の例には、コントロールが編集可能か必須かなどです。 
  
コントロール構造 **(PR_CONTROL_STRUCTURE)** には、特定の種類のコントロールに関連する情報が含まれる。 各種類のコントロールについて、異なる構造で説明します。 たとえば、編集コントロールについては [、DTBLEDIT 構造を使用して説明](dtbledit.md) します。 **DTBLEDIT** 構造体には、コントロールに配置できる文字の数と特定の種類を一覧表示するメンバーと、コントロールに表示する値を持つプロパティを識別するプロパティ タグが含まれています。 **PR_CONTROL_STRUCTURE** バイナリ プロパティとして格納されます。 
  
コントロール識別子 **(PR_CONTROL_ID)** は、表示テーブルで説明されているダイアログ ボックス内のコントロールを一意に識別します。 **PR_CONTROL_ID** は、表示テーブルを作成するために **BuildDisplayTable** によって使用される [DTCTL](dtctl.md)構造体の *lpbNotif* メンバーおよび *cbNotif* メンバーに配置された値から設定されます。 MAPI は表示テーブルを組み合わせPR_CONTROL_ID **一意** である必要があります。 通常、プロバイダーは GUID 構造を [ユーザーに割](guid.md) り **当PR_CONTROL_ID一** 意性を確保します。 PR_CONTROL_IDテーブル **通知** が生成されると、TABLE_NOTIFICATION [プロパティが](table_notification.md) 構造に含まれます。 
  
表示テーブルの詳細については、「表示テーブルの実装 [」および「](display-table-implementation.md) テーブル通知の表示 [について」を参照してください](about-display-table-notifications.md)。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

