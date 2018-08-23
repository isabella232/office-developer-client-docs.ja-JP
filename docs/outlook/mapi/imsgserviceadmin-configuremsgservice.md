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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a599a6fe5093e52e50d33a1761df5689b7335138
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568295"
---
# <a name="imsgserviceadminconfiguremsgservice"></a>IMsgServiceAdmin::ConfigureMsgService

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ サービスを再構成します。
  
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

 _lpUID_
  
> [in]メッセージ サービス構成の一意の識別子を格納する[MAPIUID](mapiuid.md)構造体へのポインター。 
    
 _ulUIParam_
  
> [in]構成のプロパティ シートの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> [in]プロパティ シートの表示を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> 渡された文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
MSG_SERVICE_UI_READ_ONLY 
  
> メッセージ サービスは、構成のプロパティ シートを表示する必要がありますですが、それを変更するユーザーを有効にします。 メッセージ サービスのほとんどは、このフラグを無視します。
    
SERVICE_UI_ALLOWED 
  
> メッセージ サービスは、サービスが完全に構成されていない場合にのみ、構成プロパティ シートを表示する必要があります。
    
SERVICE_UI_ALWAYS 
  
> メッセージ サービスは、[設定] プロパティ シートを常に表示する必要があります。 SERVICE_UI_ALWAYS が設定されていない SERVICE_UI_ALLOWED を設定し、 _lpProps_パラメーターで、プロパティ値の配列の有効な構成情報がない場合、[設定] プロパティ シートが表示されます。 プロパティ シートを表示するのには、SERVICE_UI_ALLOWED または SERVICE_UI_ALWAYS のいずれかを設定しなければなりません。 
    
 _あう_
  
> [in]_LpProps_が指す[SPropValue](spropvalue.md)構造体のプロパティ値の数です。 
    
 _lpProps_
  
> [in]プロパティ シートに表示するプロパティを記述するプロパティ値の配列へのポインター。 ユーザー インターフェイスを持たないメッセージ サービスを構成する必要がある場合、 _lpProps_パラメーターは NULL をしないでください。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージ サービスが正常に構成されました。
    
MAPI_E_EXTENDED_ERROR 
  
> メッセージ サービスに固有のエラーです。 エラーを説明する[MAPIERROR](mapierror.md)構造体を取得するには、クライアント アプリケーションは、 [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md)メソッドを呼び出す必要があります。 
    
MAPI_E_NOT_FOUND 
  
> メッセージの既存のサービスの_lpUID_で示される**MAPIUID**が一致しません。 
    
MAPI_E_NOT_INITIALIZED 
  
> メッセージ サービスには、エントリ ポイント関数がありません。
    
MAPI_E_USER_CANCEL 
  
> ユーザー操作がキャンセルされました、通常プロパティ シートで [**キャンセル**] ボタンをクリックするとします。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin::ConfigureMsgService**メソッドは、構成のプロパティ シートの有無にかかわらず、設定するメッセージ サービスを使用できます。 
  
プロパティ シートを表示せずに構成できるように、メッセージ サービスは通常、すべての必須および省略可能なプロパティとその値の定数を含むヘッダー ファイルの準備をします。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージ サービスを構成するのには、構造体の**MAPIUID**を取得するには、メッセージ サービスのテーブルの行のメッセージ サービスから**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) の列を取得します。 詳細については、 [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)メソッドで説明する手順を参照してください。 
  
設定するプロパティの値に関する情報を事前にある場合にのみユーザーにプロパティ シートを表示せず、メッセージ サービスを構成できます。 プロパティ シートを表示せず、メッセージ サービスを構成する場合、 _lpProps_パラメーターに有効なプロパティの値を渡すし、MSG_SERVICE_UI_READ_ONLY、SERVICE_UI_ALLOWED、または SERVICE_UI_ALWAYS フラグを設定しません。 
  
プロパティ シートを使用してユーザーの構成情報の一部またはすべてを受信する場合は、 _ulFlags_で SERVICE_UI_ALLOWED を設定します。 既定の設定を確立するためだけに既存のプロパティ情報を使用すると、ユーザー設定を変更することは、 _ulFlags_で SERVICE_UI_ALWAYS を設定します。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI では、 **IMsgServiceAdmin::ConfigureMsgService**メソッドを使用して、プロファイルに追加されたサービスを構成します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[SPropValue](spropvalue.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

