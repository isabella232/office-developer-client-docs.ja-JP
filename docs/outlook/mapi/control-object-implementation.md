---
title: コントロール オブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5484aeca5b09578fbfb6dd4758217b98cba9ac67
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611028"
---
# <a name="control-object-implementation"></a>コントロール オブジェクトの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)インターフェイスをサポートするコントロール オブジェクトまたはオブジェクトは、MAPI ダイアログ ボックスに表示されるボタンに機能を追加するためにプロバイダーによって実装されます。 コントロール オブジェクトはボタンにのみ実装できます。 
  
 **IMAPIControl には**[、GetLastError、GetState、](imapicontrol-getlasterror.md)[および](imapicontrol-getstate.md)Activate の 3 つのメソッド [があります](imapicontrol-activate.md)。 
  
MAPI は **GetState を** 呼び出して、ボタンを無効にするかどうかを決定します。 **GetState は** 、次の状況で呼び出されます。 
  
- ボタンが表示されるダイアログ ボックスが最初に表示される場合。
    
- ボタンに対して表示テーブル通知が発行された場合。 
    
ユーザーがボタンを操作できないMAPI_DISABLED操作できる場合は  _、lpulState_ パラメーター MAPI_ENABLEDに設定します。 
  
ユーザーがボタンをクリックすると、MAPI は Activate を呼び **出します**。 **[アクティブ** 化] ボタンに関連付けられているタスクを実行します。 このタスクは、ダイアログ ボックスの表示やプロパティの更新など、プロバイダーに適したタスクです。 ユーザーが取り消したため、タスクが失敗した場合は、タスクをMAPI_E_USER_CANCEL。 その他のエラーの原因については、適切なエラー値を返します。 
  
タスクが成功し、ダイアログ ボックスの別のコントロールに反映されるプロパティの変更にリンクされている場合は [、ITableData::HrNotify を呼び出します](itabledata-hrnotify.md)。 **HrNotify は**、変更されたプロパティの PR_CONTROL_ID **(** [PidTagControlId](pidtagcontrolid-canonical-property.md)) プロパティを持つ表示テーブル通知を [TABLE_NOTIFICATIONします。](table_notification.md) 構造体に新しいプロパティ値を配置しない。代わりに [、IMAPIProp::GetProps](imapiprop-getprops.md) が呼び出された場合に返します。 通常、表示テーブル通知を使用してコントロールを無効または有効にすることはできませんが、ボタンと一緒に使用できます。 MAPI は、変更されたコントロールを更新して通知に応答します。 
  
MAPI は、コントロールの **GetLastError** メソッドを呼び出します **。Activate** は、コントロール以外のエラーをMAPI_E_USER_CANCEL。 **GetLastError が** _lppMAPIError_ パラメーターの内容で返す [MAPIERROR](mapierror.md)構造体に拡張エラー情報を入れた場合、MAPI はユーザーに対してそれを表示します。 
  
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)

