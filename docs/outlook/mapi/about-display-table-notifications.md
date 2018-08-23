---
title: テーブル通知の表示について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 085151e9-4809-4d2b-ae4d-e318355e1f5a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a696357c97a85442bbfd5532892c06d570f6367c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799599"
---
# <a name="about-display-table-notifications"></a>テーブル通知の表示について

**適用対象**: Outlook 
  
表示テーブルの通知は、MAPI に表示された表の作成を担当するサービス ・ プロバイダーが送信されます。 MAPI は、表示テーブルの[IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出すと、テーブルの変更イベントを指定することによって、これらの通知を登録します。 
  
同様に、テーブルのすべての通知は、表示テーブルの通知には、 [TABLE_NOTIFICATION](table_notification.md)構造体が含まれます。 の**ulTableEvent**しかし、この構造体の**propIndex**メンバーは重要です。他のメンバーは無視されます。 **UlTableEvent**メンバーは、TABLE_ROW_MODIFIED に設定されてし、 **propIndex**メンバーは、 **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) の列の対応する行の値に設定します。 MAPI は、コントロールに表示されるプロパティの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すことによって、新しい値を表示することで、通知に応答します。 
  
テーブルの通知を表示] ダイアログ ボックスに関連するコントロールへの変更を調整するためサービス ・ プロバイダーが使用できます。 [] ダイアログ ボックスの 1 つまたは複数のフィールドを更新するのには、プロパティのインターフェイスの実装が必要な場合など、- **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) プロパティに DT_SET_IMMEDIATE フラグを設定するには別のコントロールへの応答ではおそらく、テーブルの通知を表示を生成できます。 テーブルの通知を表示には、1 つまたは複数のコントロールの値を変更するために再読み込みする必要があるプロパティのインターフェイスの実装や、外部イベントの発生を警告できます。 
  
サービス プロバイダーは、表示テーブルの通知を発行できます。
  
- 表示テーブルがテーブルのデータ オブジェクトを使用してビルドされている場合は、 [ITableData::HrNotify](itabledata-hrnotify.md)を呼び出しています。
    
    - または、
    
- **IMAPITable**プロバイダーに表示された表を作成した場合は、独自のコードを使用しています。 
    
MAPI は、プロパティのインターフェイスの実装からのコントロールの値を再読み取りが必要な場合に通知を表を表示するのに応答します。 次の表では、MAPI がコントロールの特定の種類の通知を処理する方法に関する詳細について説明します。
  
|**Control**|**MAPI 操作**|
|:-----|:-----|
|ボタン  <br/> |呼び出しが以前に失敗した場合に、 **ulPRControl** 、 [DTBLBUTTON](dtblbutton.md)構造体のメンバーによって表されるプロパティを使用してコントロール オブジェクトを取得するために[IMAPIProp::OpenProperty](imapiprop-openproperty.md)を呼び出します。 かを判断、ボタンを有効にしてにより、それに応じて、ボタンを無効にするのには、コントロール オブジェクトの[IMAPIControl::GetState](imapicontrol-getstate.md)を呼び出します。  <br/> |
|チェック ボックス  <br/> |**UlPRPropertyName**メンバーの値を再読み込みします。  <br/> |
|コンボ ボックス  <br/> |**UlPRTableName** 、 [DTBLCOMBOBOX](dtblcombobox.md)構造体のメンバーに関連付けられているテーブルを再度開きます。 すべての**ulPRPropertyName**メンバーの値を含む行を再読み込みします。  <br/> |
|ドロップダウン リスト ボックス  <br/> |**UlPRTableName** 、 [DTBLDDLBX](dtblddlbx.md)構造体のメンバーに関連付けられているテーブルを再度開き、すべての行を再読み込みします。 **UlPRDisplayProperty**と**ulPRSetProperty**のメンバーに格納されているプロパティの値を取得するために[IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出します。  <br/> |
|編集  <br/> |プロパティを再読み込みし、再表示します。  <br/> |
|グループ ボックス  <br/> |通知を無視します。  <br/> |
|ラベル  <br/> |通知を無視します。  <br/> |
|複数選択リスト ボックス  <br/> |エントリ識別子列のいずれかの場合は、リスト ボックスを更新します。 対応するオブジェクトがクローズまたは再読み込みされません。  <br/> |
|単一選択リスト ボックス  <br/> |識別しようとして、セットのプロパティを読み取ります。  <br/> |
|複数値を持つリスト ボックス  <br/> |プロパティを再読み込みし、リスト ボックスを再設定します。  <br/> |
|タブ付きページ  <br/> |このコントロールでの通知はありません。すべてが静的です。  <br/> |
|ラジオ ボタン  <br/> |ボタンに関連付けられていると、 **ulPropTag** 、 [DTBLRADIOBUTTON](dtblradiobutton.md)構造体のメンバーに格納されて、コントロールの適切な選択では、プロパティを再読み込みします。  <br/> |
   
## <a name="see-also"></a>関連項目

- [MAPI テーブル](mapi-tables.md)

