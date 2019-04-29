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
  
表示テーブルの通知は、MAPI への表示テーブルの作成を担当するサービスプロバイダーによって送信されます。 MAPI は、表示テーブルの[IMAPITable:: Advise](imapitable-advise.md)メソッドを呼び出して、テーブルの変更イベントを指定することにより、これらの通知に対して登録します。 
  
すべてのテーブル通知と同様に、表示テーブル通知には[TABLE_NOTIFICATION](table_notification.md)構造が含まれています。 この構造体の**ultableevent**および**propindex**メンバーのみが重要です。その他のメンバーは無視されます。 **ultableevent**メンバーは TABLE_ROW_MODIFIED に設定されており、 **propindex**メンバーは対応する行の**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) 列の値に設定されています。 MAPI は通知に応答します。このメソッドは、コントロールに表示されるプロパティと新しい値を表示するために、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出します。 
  
表示テーブル通知は、サービスプロバイダーがダイアログボックスの関連するコントロールに対する変更を調整するために使用できます。 たとえば、プロパティインターフェイスの実装で、ダイアログボックスの1つ以上のフィールドを更新する必要がある場合 (たとえば、 **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) プロパティに DT_SET_IMMEDIATE フラグが設定されている別のコントロールに応答する場合など)。表示テーブル通知を生成できます。 表示テーブル通知は、変更が行われたり、外部イベントが発生したりすることによって、1つ以上のコントロールの値を再読み込みする必要があることを、プロパティインターフェイスの実装に対して通知できます。 
  
サービスプロバイダーは、次の方法で表示テーブル通知を発行できます。
  
- テーブルデータオブジェクトを使用して表示テーブルが作成されている場合は、 [itabledata:: hrnotify](itabledata-hrnotify.md)を呼び出します。
    
    - や
    
- プロバイダーの**IMAPITable**実装で表示テーブルが作成されている場合は、独自のコードを使用します。 
    
MAPI は、必要に応じて、プロパティインターフェイスの実装からコントロールの値を再度読み込みすることで、テーブル通知の表示に応答します。 次の表では、特定の種類のコントロールについて MAPI が通知を処理する方法について詳しく説明します。
  
|**Control**|**MAPI アクション**|
|:-----|:-----|
|ボタン  <br/> |[imapiprop:: openproperty](imapiprop-openproperty.md)を呼び出して、呼び出しが以前に失敗した場合に、 [dtblbutton](dtblbutton.md)構造の**ulprcontrol**メンバーによって表されるプロパティによって制御オブジェクトを取得します。 コントロールオブジェクトの[IMAPIControl:: GetState](imapicontrol-getstate.md)を呼び出して、ボタンを有効にする必要があるかどうかを判断し、それに応じてボタンを有効または無効にします。  <br/> |
|チェック ボックス  <br/> |**ulprpropertyname**メンバーの値を再度読み込みます。  <br/> |
|コンボ ボックス  <br/> |[dtblcombobox](dtblcombobox.md)構造体の**ulprtablename**メンバーに関連付けられているテーブルを再度開きます。 **ulprpropertyname**メンバーの値を含むすべての行を再度読み込みます。  <br/> |
|ドロップダウンリストボックス  <br/> |[dtblddlbx](dtblddlbx.md)構造の**ulprtablename**メンバーに関連付けられているテーブルを再度開き、すべての行を再度読み込みます。 [imapiprop:: GetProps](imapiprop-getprops.md)を呼び出して、 **ulprdisplayproperty**および**ulprsetproperty**メンバーに格納されているプロパティの値を取得します。  <br/> |
|Edit  <br/> |プロパティを再度読み込み、再読み込みします。  <br/> |
|グループ ボックス  <br/> |通知を無視します。  <br/> |
|Label  <br/> |通知を無視します。  <br/> |
|複数選択リストボックス  <br/> |いずれかの列がエントリ識別子の場合は、リストボックスを更新します。 対応するオブジェクトが閉じられていないか、再読み込みになっていません。  <br/> |
|単一選択リストボックス  <br/> |set プロパティを読み取り、それを識別します。  <br/> |
|複数値リストボックス  <br/> |プロパティを再度読み込み、リストボックスに再読み込みします。  <br/> |
|タブ付きページ  <br/> |このコントロールには通知がありません。すべては静的です。  <br/> |
|ラジオボタン  <br/> |ボタンに関連付けられているプロパティを再度読み込み、 [dtblradiobutton](dtblradiobutton.md)構造の**ulPropTag**メンバーに格納して、コントロールで適切な選択を行います。  <br/> |
   
## <a name="see-also"></a>関連項目

- [MAPI テーブル](mapi-tables.md)

