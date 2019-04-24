---
title: コントロールオブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8304021565638f8a5893d0be8cd6a94ed62a8d95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335659"
---
# <a name="control-object-implementation"></a>コントロールオブジェクトの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コントロールオブジェクト、または[IMAPIControl: IUnknown](imapicontroliunknown.md)インターフェイスをサポートするオブジェクトは、プロバイダーによって実装され、MAPI ダイアログボックスに表示されるボタンに機能を追加します。 コントロールオブジェクトは、ボタンに対してのみ実装できます。 
  
 **IMAPIControl**には、 [GetLastError](imapicontrol-getlasterror.md)、 [GetState](imapicontrol-getstate.md)、および[Activate](imapicontrol-activate.md)の3つのメソッドがあります。 
  
MAPI は**GetState**を呼び出して、ボタンを無効にするかどうかを判断します。 **GetState**は、次のような場合に呼び出されます。 
  
- ボタンが表示されるダイアログボックスが最初に表示されます。
    
- ボタンに対して表示テーブル通知が発行されたとき。 
    
ユーザーが操作できる場合は、ボタンと MAPI_ENABLED を操作できない場合は、 _lMAPI_DISABLED state_パラメーターの内容を「」に設定します。 
  
ユーザーがボタンをクリックすると、MAPI 呼び出しが**アクティブ**になります。 **Activate**は、ボタンに関連付けられているタスクを実行します。 このタスクは、ダイアログボックスを表示したり、プロパティを更新したりするなど、プロバイダーにとって適切なものでもかまいません。 ユーザーがキャンセルしたためにタスクが失敗した場合は、MAPI_E_USER_CANCEL を返します。 失敗のその他の原因については、適切なエラー値を返します。 
  
タスクが正常に実行され、ダイアログボックスの別のコントロールに反映されるプロパティの変更にリンクされている場合は、 [itabledata:: hrnotify](itabledata-hrnotify.md)を呼び出します。 **hrnotify**は、 [TABLE_NOTIFICATION](table_notification.md)構造の変更されたプロパティの**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) プロパティを使用して、表示テーブル通知を発行するために呼び出されます。 新しいプロパティの値は、構造体に配置しないでください。代わりに、 [imapiprop:: GetProps](imapiprop-getprops.md)が呼び出されたときに返されます。 通常、表示テーブル通知を使用してコントロールを無効または有効にすることはできませんが、ボタンと共に使用することができます。 MAPI は、通知に応答するように変更されたコントロールを更新します。 
  
MAPI は、**アクティブ化**時に MAPI_E_USER_CANCEL 以外のエラーを返すコントロールの**GetLastError**メソッドを呼び出します。 **GetLastError**が、 _lppMAPIError_パラメーターの内容で返される[MAPIERROR](mapierror.md)構造に拡張エラー情報を配置すると、ユーザーに対して MAPI に表示されます。 
  
## <a name="see-also"></a>関連項目



[MAPI サービスプロバイダー](mapi-service-providers.md)

