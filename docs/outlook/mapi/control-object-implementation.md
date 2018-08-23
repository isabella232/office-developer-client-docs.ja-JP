---
title: コントロール オブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 268ad60cf8161fb2b58370f89aae623aabd7da7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799826"
---
# <a name="control-object-implementation"></a>コントロール オブジェクトの実装

  
  
**適用対象**: Outlook 
  
オブジェクト、またはサポートしているオブジェクトを制御する、 [IMAPIControl: IUnknown](imapicontroliunknown.md)インタ フェースで、MAPI ダイアログ ボックスに表示されるボタンに機能を追加するのにはプロバイダーによって実装されます。 コントロール オブジェクトは、ボタンの場合にのみ実装できます。 
  
 **IMAPIControl**には 3 つの方法:[発生しました](imapicontrol-getlasterror.md)、 [GetState](imapicontrol-getstate.md)、および[アクティブ化](imapicontrol-activate.md)します。 
  
MAPI では、ボタンを無効にするかどうかを判断するのには、 **GetState**を呼び出します。 **GetState**は、次の状況で呼び出されます。 
  
- ボタンを表示するダイアログ ボックスが最初に表示されます。
    
- テーブルの通知を表示は、ボタンに対して実行されます。 
    
操作すること、ボタンと MAPI_ENABLED 場合は、ユーザーが対話できる場合は、 _lpulState_パラメーターの内容を MAPI_DISABLED に設定します。 
  
ユーザーは、ボタンをクリックすると、MAPI は、**ライセンス認証を行う**を呼び出します。 **アクティブにする**には、ボタンに関連付けられているタスクが実行されます。 このタスクは、プロバイダーには、ダイアログ ボックスを表示する、プロパティを更新するなど、適切なものにできます。 タスクが失敗した場合、ユーザーがキャンセルされたため、MAPI_E_USER_CANCEL を返します。 障害の原因は他の適切なエラー値を返します。 
  
タスクが成功し、プロパティの変更] ダイアログ ボックスで別のコントロールに反映されるにリンクされている場合は、 [ITableData::HrNotify](itabledata-hrnotify.md)を呼び出します。 **HrNotify**は、 [TABLE_NOTIFICATION](table_notification.md)構造体の**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) プロパティがプロパティの変更の通知を表示テーブルを発行するために呼び出されます。 構造に新しいプロパティの値を配置しません。代わりに、 [IMAPIProp::GetProps](imapiprop-getprops.md)が呼び出されたときに、それを返します。 通常、コントロールを有効または無効にするテーブルの通知を表示を使用することはできませんは、ボタンを使用できます。 MAPI 通知への応答に変更されたコントロールが更新されます。 
  
MAPI**をアクティブにする**には、MAPI_E_USER_CANCEL 以外のエラーが返されるときに、コントロールの**GetLastError**メソッドを呼び出します。 _LppMAPIError_パラメーターの内容で返される[MAPIERROR](mapierror.md)構造体に**発生しました**がエラーの詳細情報を置くと、ユーザーの MAPI 表示します。 
  
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)

