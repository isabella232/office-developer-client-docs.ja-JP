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
  
> [in]構成するメッセージ サービスの一意の識別子を含む [MAPIUID](mapiuid.md) 構造体へのポインター。 
    
 _ulUIParam_
  
> [in]構成プロパティ シートの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> [in]プロパティ シートの表示を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
MSG_SERVICE_UI_READ_ONLY 
  
> メッセージ サービスは構成プロパティ シートを表示しますが、ユーザーが変更を有効にしない必要があります。 ほとんどのメッセージ サービスでは、このフラグは無視されます。
    
SERVICE_UI_ALLOWED 
  
> メッセージ サービスは、サービスが完全に構成されていない場合にのみ、構成プロパティ シートを表示する必要があります。
    
SERVICE_UI_ALWAYS 
  
> メッセージ サービスは常に構成プロパティ シートを表示する必要があります。 このSERVICE_UI_ALWAYS設定されていない場合、SERVICE_UI_ALLOWED が設定されている場合でも  _、lpProps_ パラメーターのプロパティ値配列から有効な構成情報を使用できない場合は、構成プロパティ シートを表示できます。 プロパティ SERVICE_UI_ALLOWED表示SERVICE_UI_ALWAYS設定する必要があります。 
    
 _cValues_
  
> [in]lpProps が指す [SPropValue](spropvalue.md) 構造体のプロパティ値  _の数_ です。 
    
 _lpProps_
  
> [in]プロパティ シートに表示するプロパティを表すプロパティ値の配列へのポインター。 メッセージ サービスをユーザー インターフェイスなしで構成する必要がある場合は  _、lpProps_ パラメーターを NULL にすることはできません。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージ サービスが正常に構成されました。
    
MAPI_E_EXTENDED_ERROR 
  
> メッセージ サービスに固有のエラー。 エラーを [説明する MAPIERROR](mapierror.md) 構造を取得するには、クライアント アプリケーションが [IMsgServiceAdmin::GetLastError メソッドを呼び出す必要](imsgserviceadmin-getlasterror.md) があります。 
    
MAPI_E_NOT_FOUND 
  
> lpUID が指す _MAPIUID_ は、既存のメッセージ サービスの **MAPIUID** と一致しません。 
    
MAPI_E_NOT_INITIALIZED 
  
> メッセージ サービスにエントリ ポイント関数はありません。
    
MAPI_E_USER_CANCEL 
  
> ユーザーは、通常、プロパティ シートの [キャンセル] ボタンをクリック **して、操作** を取り消しました。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin::ConfigureMsgService** メソッドを使用すると、構成プロパティ シートの付きまたは指定なしでメッセージ サービスを構成できます。 
  
プロパティ シートを表示せずに構成を許可するには、通常、メッセージ サービスは、必要なすべてのプロパティとオプションのプロパティとその値の定数を含むヘッダー ファイルを準備します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

構成するメッセージ サービスの **MAPIUID** 構造を取得するには、メッセージ サービス テーブルのメッセージ サービスの行から **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) 列を取得します。 詳細については [、「IMsgServiceAdmin::CreateMsgService メソッド」で説明されている手順を参照](imsgserviceadmin-createmsgservice.md) してください。 
  
設定するプロパティ値に関する事前情報がある場合にのみ、ユーザーにプロパティ シートを表示せずにメッセージ サービスを構成できます。 プロパティ シートを表示せずにメッセージ サービスを構成する場合は  _、lpProps_ パラメーターに有効なプロパティ値を渡し、MSG_SERVICE_UI_READ_ONLY、SERVICE_UI_ALLOWED、または SERVICE_UI_ALWAYS フラグを設定しない。 
  
プロパティ シートを使用してユーザーから構成情報のすべてまたは一部を受け取る場合は  _、ulFlags_ にSERVICE_UI_ALLOWED設定します。 既存のプロパティ情報のみを使用して既定の設定を確立し、ユーザーが設定を変更できる場合は  _、ulFlags_ で SERVICE_UI_ALWAYSを設定します。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI は **、IMsgServiceAdmin::ConfigureMsgService** メソッドを使用して、プロファイルに追加されたサービスを構成します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[SPropValue](spropvalue.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

