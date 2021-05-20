---
title: テーブル通知の表示について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 085151e9-4809-4d2b-ae4d-e318355e1f5a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 41e6a2c8b6856bf072972325e7e08aabe3e17446
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430015"
---
# <a name="about-display-table-notifications"></a>テーブル通知の表示について

**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルの通知は、MAPI への表示テーブルの作成を担当するサービス プロバイダーによって送信されます。 MAPI は、表示テーブルの [IMAPITable::Advise](imapitable-advise.md) メソッドを呼び出し、テーブル変更イベントを指定することで、これらの通知を登録します。 
  
すべてのテーブル通知と同様に、表示テーブル通知には[、TABLE_NOTIFICATIONがあります。](table_notification.md) この構造体 **の ulTableEvent** メンバー **と propIndex** メンバーだけが重要です。他のメンバーは無視されます。 **ulTableEvent** メンバーは TABLE_ROW_MODIFIED に設定され **、propIndex** メンバーは対応する行の **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) 列の値に設定されます。 MAPI は、コントロールに表示されるプロパティの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出し、新しい値を表示することで通知に応答します。 
  
表示テーブル通知は、サービス プロバイダーがダイアログ ボックスで関連するコントロールへの変更を調整するために使用できます。 たとえば、プロパティ インターフェイスの実装でダイアログ ボックスの 1 つ以上のフィールドを更新する必要がある場合 (PR_CONTROL_FLAGS ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) プロパティで **DT_SET_IMMEDIATE** フラグを設定した別のコントロールに応答して、表示テーブル通知を生成できます。 表示テーブル通知は、変更が行われたり、外部イベントが発生したりして、1 つ以上のコントロールの値を再読み取りする必要があるというプロパティ インターフェイスの実装を通知できます。 
  
サービス プロバイダーは、次の方法で表示テーブル通知を発行できます。
  
- 表示テーブルがテーブル データ オブジェクトで構築されている場合は [、ITableData::HrNotify](itabledata-hrnotify.md)を呼び出します。
    
    - Or -
    
- プロバイダーの IMAPITable 実装で表示テーブルが構築されている場合は、独自 **のコードを使用** します。 
    
MAPI は、プロパティ インターフェイスの実装からコントロールの値を再読み取りすることで、必要に応じてテーブル通知の表示に応答します。 次の表では、MAPI が特定の種類のコントロールの通知を処理する方法の詳細について説明します。
  
|**Control**|**MAPI アクション**|
|:-----|:-----|
|ボタン  <br/> |[IMAPIProp::OpenProperty](imapiprop-openproperty.md)を呼び出して、以前に呼び出しが失敗した場合に [DTBLBUTTON](dtblbutton.md)構造体の **ulPRControl** メンバーによって表されるプロパティを使用してコントロール オブジェクトを取得します。 コントロール オブジェクトの [IMAPIControl::GetState](imapicontrol-getstate.md) を呼び出して、ボタンを有効にし、ボタンを適切に有効または無効にするかどうかを決定します。  <br/> |
|チェック ボックス  <br/> |**ulPRPropertyName メンバーの値を再読み取** りします。  <br/> |
|コンボ ボックス  <br/> |[DTBLCOMBOBOX](dtblcombobox.md)構造体の **ulPRTableName** メンバーに関連付けられているテーブルを再度開きます。 **ulPRPropertyName** メンバーの値を含むすべての行を再読み込みします。  <br/> |
|ドロップダウン リスト ボックス  <br/> |[DTBLDDLBX](dtblddlbx.md)構造体の **ulPRTableName** メンバーに関連付けられているテーブルを再度開き、すべての行を再読み込みします。 [IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出して **、ulPRDisplayProperty** および **ulPRSetProperty** メンバーに格納されているプロパティの値を取得します。  <br/> |
|編集  <br/> |プロパティを再読み込みし、再表示します。  <br/> |
|グループ ボックス  <br/> |通知を無視します。  <br/> |
|ラベル  <br/> |通知を無視します。  <br/> |
|複数の選択リスト ボックス  <br/> |列の 1 つがエントリ識別子の場合は、リスト ボックスを更新します。 対応するオブジェクトは閉じても再読み込みもされません。  <br/> |
|単一選択リスト ボックス  <br/> |set プロパティを読み取り、それを識別します。  <br/> |
|複数値リスト ボックス  <br/> |プロパティを再読み込みし、リスト ボックスを再設定します。  <br/> |
|タブ付きページ  <br/> |このコントロールの通知はありません。すべてが静的です。  <br/> |
|ラジオ ボタン  <br/> |ボタンに関連付けられているプロパティを再読み取りし [、DTBLRADIOBUTTON](dtblradiobutton.md)構造体の **ulPropTag** メンバーに格納され、コントロールで適切な選択を行います。  <br/> |
   
## <a name="see-also"></a>関連項目

- [MAPI テーブル](mapi-tables.md)

