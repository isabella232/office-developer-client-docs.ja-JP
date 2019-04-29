---
title: IMsgServiceAdminConfigureMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.ConfigureMsgService
api_type:
- COM
ms.assetid: a08f5905-2585-49ca-abb7-a77f2736f604
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 87ac394f9ab77b092cdfcd44f65b040a039319e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422188"
---
# <a name="imsgserviceadminconfiguremsgservice"></a>IMsgServiceAdmin::ConfigureMsgService

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージサービスを再構成します。
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>パラメーター

 _lpuid_
  
> 順番構成するメッセージサービスの一意の識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。 
    
 _uluiparam_
  
> 順番構成プロパティシートの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> 順番プロパティシートの表示を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
MSG_SERVICE_UI_READ_ONLY 
  
> メッセージサービスには、その構成プロパティシートが表示されますが、ユーザーが変更することはできません。 ほとんどのメッセージサービスでは、このフラグは無視します。
    
SERVICE_UI_ALLOWED 
  
> サービスが完全に構成されていない場合にのみ、メッセージサービスにその構成プロパティシートが表示されます。
    
SERVICE_UI_ALWAYS 
  
> メッセージサービスには、常にその構成プロパティシートが表示されている必要があります。 SERVICE_UI_ALWAYS が設定されていない場合でも、SERVICE_UI_ALLOWED が設定されていて、有効な構成情報が_lpprops_パラメーターのプロパティ値の配列から利用できない場合、構成プロパティシートが表示されることがあります。 プロパティシートが表示されるようにするには、SERVICE_UI_ALLOWED または SERVICE_UI_ALWAYS のいずれかを設定する必要があります。 
    
 _cvalues_
  
> 順番_lpprops_によってポイントされた[spropvalue](spropvalue.md)構造のプロパティ値の数。 
    
 _lpprops_
  
> 順番プロパティシートに表示されるプロパティを説明するプロパティ値の配列へのポインター。 メッセージサービスをユーザーインターフェイスなしで構成する必要がある場合は、 _lpprops_パラメーターを NULL にしないでください。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージサービスが正常に構成されました。
    
MAPI_E_EXTENDED_ERROR 
  
> メッセージサービスに固有のエラー。 エラーを説明する[MAPIERROR](mapierror.md)構造を取得するには、クライアントアプリケーションは[IMsgServiceAdmin:: GetLastError](imsgserviceadmin-getlasterror.md)メソッドを呼び出す必要があります。 
    
MAPI_E_NOT_FOUND 
  
> _lpuid_が指す**MAPIUID**が、既存のメッセージサービスのものと一致しません。 
    
MAPI_E_NOT_INITIALIZED 
  
> メッセージサービスにエントリポイント関数がありません。
    
MAPI_E_USER_CANCEL 
  
> ユーザーが操作をキャンセルしました。通常は、プロパティシートの **[キャンセル**] ボタンをクリックします。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin:: ConfigureMsgService**メソッドを使用すると、構成プロパティシートの有無にかかわらず、メッセージサービスを構成できます。 
  
プロパティシートが表示されない構成を許可する場合、通常、メッセージサービスは、必要なすべてのプロパティとその値の定数を含むヘッダーファイルを準備します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

構成するメッセージサービスの**MAPIUID**構造を取得するには、メッセージサービステーブルのメッセージサービスの行から [ **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))] 列を取得します。 詳細については、 [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md)メソッドに記載されている手順を参照してください。 
  
設定するプロパティ値に関する詳細情報がある場合にのみ、ユーザーにプロパティシートを表示せずに、メッセージサービスを構成できます。 プロパティシートを表示せずにメッセージサービスを構成する場合は、 _lpprops_パラメーターに有効なプロパティ値を渡し、MSG_SERVICE_UI_READ_ONLY、SERVICE_UI_ALLOWED、または SERVICE_UI_ALWAYS フラグは設定しません。 
  
プロパティシートを使用して、ユーザーから構成情報の全部または一部を受け取った場合は、 _ulflags_で SERVICE_UI_ALLOWED を設定します。 既存のプロパティ情報のみを使用して既定の設定を確立し、ユーザーが設定を変更できる場合は、 _ulflags_で SERVICE_UI_ALWAYS を設定します。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProfileFunctions  <br/> |hraddservicetoprofile  <br/> |mfcmapi は、 **IMsgServiceAdmin:: ConfigureMsgService**メソッドを使用して、プロファイルに追加されたサービスを構成します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[SPropValue](spropvalue.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

