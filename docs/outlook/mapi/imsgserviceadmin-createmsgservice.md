---
title: IMsgServiceAdminCreateMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.CreateMsgService
api_type:
- COM
ms.assetid: 0135f049-0311-45e5-9685-78597d599a4e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0b3d8327607db0546a4737cdddb3d913e54077eb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579874"
---
# <a name="imsgserviceadmincreatemsgservice"></a>IMsgServiceAdmin::CreateMsgService

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
非推奨: [IMsgServiceAdmin2::CreateMsgServiceEx の使用をお](imsgserviceadmin2-createmsgserviceex.md) 勧めします。 現在のプロファイルにメッセージ サービスを追加します。 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>パラメーター

 _lpszService_
  
> [in]追加するメッセージ サービスの名前へのポインター。 このメッセージ サービス名は、MapiSvc.inf ファイル **の [Services]** セクションに表示される必要があります。 
    
 _lpszDisplayName_
  
> [in]追加するメッセージ サービスの表示名へのポインター。 メッセージ サービスが MapiSvc.inf ファイルの PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを設定している場合 _、lpszDisplayName_ パラメーターは無視されます。
    
 _ulUIParam_
  
> [in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> [in]メッセージ サービスのインストール方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE
  
> lpszService パラメーターと lpszDisplayName パラメーターを LPWSTR にキャストし、Unicode 文字列として解釈する必要があります。
    
SERVICE_NO_RESTART_WARNING
  
> プロファイルに新しいメッセージ サービスを追加する場合、MAPI サブシステムは、さまざまな状況と条件に基づいて、多くの場合、このアクションでプロファイルの再起動が必要Outlook。 SERVICE_NO_RESTART_WARNING フラグが含まれていない場合に、SERVICE_UI_ALWAYS フラグと SERVICE_UI_ALLOWED フラグに基づいて UI が許可され、少なくとも 1 つのプロセスが現在のプロファイルにログオンしている場合、この関数は「これらの変更を有効にするために Outlook を再起動する必要があります」というメッセージを表示します。 フラグをSERVICE_NO_RESTART_WARNINGすると、その警告メッセージの表示が抑制されます。
    
SERVICE_UI_ALLOWED
  
> 必要に応じて、メッセージ サービス構成 UI を使用できます。
    
SERVICE_UI_ALWAYS 
  
> メッセージ サービスは、構成プロパティ シートを表示します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NOT_FOUND 
  
> メッセージ サービス名は MapiSvc.inf の **[Services]** セクションに含めではありません。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin::CreateMsgService** メソッドは、現在のプロファイルにメッセージ サービスを追加します。 **CreateMsgService は** 、メッセージ サービスのエントリ ポイント関数を呼び出して、サービス固有の構成タスクを実行します。 _ulFlags_ パラメーター SERVICE_UI_ALLOWEDフラグが設定されている場合、インストールされているメッセージ サービスはプロパティ シートを表示して、ユーザーが設定を構成できます。 
  
MapiSvc.inf ファイルには、メッセージ サービスを構成するプロバイダーの一覧と、それぞれのプロパティが含まれる。 **CreateMsgService** は、まずメッセージ サービスの新しいプロファイル セクションを作成し、そのサービスのすべての情報を MapiSvc.inf ファイルからプロファイルにコピーし、プロバイダーごとに新しいセクションを作成します。 
  
MapiSvc.inf からすべての情報がコピーされた後、メッセージ サービスのエントリ ポイント関数が呼び出され  _、ulContext_ パラメーターに MSG_SERVICE_CREATE 値が設定されます。 **CreateMsgService** メソッドの _ulFlags_ パラメーターで SERVICE_UI_ALLOWED フラグが設定されている場合、メッセージ サービスのエントリ ポイント関数が呼び出された場合 _、ulUIParam_ パラメーターと _ulFlags_ パラメーターの値も渡されます。 サービス プロバイダーは、ユーザーがメッセージ サービスを構成できるよう、構成プロパティ シートを表示する必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **CreateMsgService** は、プロファイルに追加されたメッセージ サービスの [MAPIUID](mapiuid.md) 構造を返します。 
  
作成したメッセージ **サービスの MAPIUID** を取得するには、次の手順を使用します。 
  
1. メッセージ サービス [管理テーブルを取得するには、IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) メソッドを呼び出します。 
    
2. メッセージ サービスの名前を持つ **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) プロパティに一致するテーブルに制限を設定して、メッセージ サービスを表す行を探します。 
    
3. サービスのプロパティ [(PidTagServiceUid)](pidtagserviceuid-canonical-property.md) **PR_SERVICE_UIDプロパティ** を取得します。 
    
4. _lpUid_ パラメーターの **PR_SERVICE_UID** プロパティの値を [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)メソッドに渡して、サービスを構成します。 
    
> [!CAUTION]
> MAPI Microsoft Outlook 2010の実装では、MAPI サブシステムMAPI_UNICODEサポートされません。使用すると失敗します。 
  
> [!IMPORTANT]
> _ulFlags_ SERVICE_NO_RESTART_WARNINGは、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。その場合は、次の値を使用してコードに追加>`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI は **、IMsgServiceAdmin::CreateMsgService** メソッドを使用して、サービスをプロファイルに追加します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

