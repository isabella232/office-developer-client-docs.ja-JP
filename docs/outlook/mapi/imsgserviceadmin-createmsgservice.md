---
title: IMsgServiceAdminCreateMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CreateMsgService
api_type:
- COM
ms.assetid: 0135f049-0311-45e5-9685-78597d599a4e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e7d30c1aba8ddc1419045c1caa8524f7d2063dc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434978"
---
# <a name="imsgserviceadmincreatemsgservice"></a>IMsgServiceAdmin::CreateMsgService

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
非推奨: [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md)を使用することをお勧めします。 現在のプロファイルにメッセージサービスを追加します。 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>パラメーター

 _lpszservice_
  
> 順番追加するメッセージサービスの名前へのポインター。 このメッセージサービス名は、mapisvc.inf ファイルの **[Services]** セクションに表示される必要があります。 
    
 _lpszdisplayname_
  
> 順番追加するメッセージサービスの表示名へのポインター。 メッセージサービスが mapisvc.inf ファイルで**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを設定している場合、 _lpszdisplayname_パラメーターは無視されます。
    
 _uluiparam_
  
> 順番このメソッドが表示する任意のダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> 順番メッセージサービスのインストール方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE
  
> lpszservice および lpszservice パラメーターは、LPWSTR にキャストし、Unicode 文字列として解釈される必要があります。
    
SERVICE_NO_RESTART_WARNING
  
> プロファイルに新しいメッセージサービスを追加すると、さまざまな状況や条件に基づいて MAPI サブシステムが、Outlook の再起動が必要であると判断されることがよくあります。 SERVICE_NO_RESTART_WARNING フラグが含まれておらず、SERVICE_UI_ALWAYS と SERVICE_UI_ALLOWED フラグに基づいて UI が許可されていて、少なくとも1つのプロセスが現在のプロファイルに記録されている場合、この関数は "Outlook を再起動する必要があります。" というメッセージを表示します。これらの変更は有効になります。 SERVICE_NO_RESTART_WARNING フラグを含めると、その警告メッセージの表示が抑制されます。
    
SERVICE_UI_ALLOWED
  
> 必要に応じて、メッセージサービス構成 UI を使用できます。
    
SERVICE_UI_ALWAYS 
  
> メッセージサービスには、その構成プロパティシートが表示されます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NOT_FOUND 
  
> メッセージサービス名が mapisvc.inf の **[Services]** セクションにありません。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin:: CreateMsgService**メソッドは、現在のプロファイルにメッセージサービスを追加します。 **CreateMsgService**は、メッセージサービスのエントリポイント関数を呼び出して、サービス固有の構成タスクを実行します。 SERVICE_UI_ALLOWED フラグが_ulflags_パラメーターで設定されている場合は、インストールされているメッセージサービスにプロパティシートを表示して、ユーザーがその設定を構成できるようにすることができます。 
  
mapisvc.inf ファイルには、メッセージサービスを構成するプロバイダーの一覧とそれぞれのプロパティが含まれています。 **CreateMsgService**は、最初にメッセージサービス用の新しいプロファイルセクションを作成し、そのサービスのすべての情報を mapisvc.inf ファイルからプロファイルにコピーして、各プロバイダーに新しいセクションを作成します。 
  
すべての情報が mapisvc.inf からコピーされた後、メッセージサービスのエントリポイント関数が、 _ulcontext_パラメーターで設定された MSG_SERVICE_CREATE 値を使用して呼び出されます。 SERVICE_UI_ALLOWED フラグが**CreateMsgService**メソッドの_ulflags_パラメーターで設定されている場合は、メッセージサービスのエントリポイント関数が呼び出されたときに、 _uluiparam_パラメーターと_ulflags_パラメーターの値も渡されます。 サービスプロバイダーは、ユーザーがメッセージサービスを構成できるように、その構成プロパティシートを表示する必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **CreateMsgService**は、プロファイルに追加されたメッセージサービスの[MAPIUID](mapiuid.md)構造を返しません。 
  
作成されたメッセージサービスの**MAPIUID**を取得するには、次の手順を使用します。 
  
1. [IMsgServiceAdmin:: getmsgservicetable](imsgserviceadmin-getmsgservicetable.md)メソッドを呼び出して、メッセージサービス管理テーブルを取得します。 
    
2. **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) プロパティとメッセージサービスの名前を一致させる制限をテーブルに配置することによって、メッセージサービスを表す行を見つけます。 
    
3. サービスの**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティを取得します。 
    
4. _lpuid_パラメーターの**PR_SERVICE_UID**プロパティの値を[IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)メソッドに渡して、サービスを構成します。 
    
> [!CAUTION]
> MAPI サブシステムの Microsoft Outlook 2010 実装は MAPI_UNICODE をサポートしていないため、使用されている場合は失敗します。 
  
> [!IMPORTANT]
> _ulflags_ SERVICE_NO_RESTART_WARNING は、現在のダウンロード可能なヘッダーファイルでは定義されていない場合があります。その場合は、次の値を使用してコードに追加できます。 >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProfileFunctions  <br/> |hraddservicetoprofile  <br/> |mfcmapi は、 **IMsgServiceAdmin:: CreateMsgService**メソッドを使用して、プロファイルにサービスを追加します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

