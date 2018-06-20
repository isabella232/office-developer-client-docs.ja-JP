---
title: IMsgServiceAdminDeleteMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.DeleteMsgService
api_type:
- COM
ms.assetid: 3a6b34eb-9d46-488f-8d02-91b27c35de67
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0a3021ed386aa00777694452a755693fc4078093
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800967"
---
# <a name="imsgserviceadmindeletemsgservice"></a>IMsgServiceAdmin::DeleteMsgService

  
  
**適用されます**: Outlook 
  
メッセージ サービスをプロファイルから削除します。
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a>Parameters

 _lpuid_
  
> [in]削除するメッセージ サービスの一意の識別子を格納する[MAPIUID](mapiuid.md)構造体へのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージ サービスが削除されました。
    
MAPI_E_NOT_FOUND 
  
> _Lpuid_で指定された**MAPIUID**では、既存のメッセージ サービスが一致しません。 
    
## <a name="remarks"></a>備考

**IMsgServiceAdmin::DeleteMsgService**メソッドは、メッセージ サービスをプロファイルから削除します。 **DeleteMsgService**は、メッセージ サービスに関連するすべてのプロファイル セクションを削除します。 
  
 **DeleteMsgService**は、メッセージ サービスを削除するのには次の手順を実行します。 
  
1. プロファイルのセクションを削除する前に MSG_SERVICE_DELETE を設定する_ulContext_パラメーターを使用して、メッセージ サービスのエントリ ポイント関数を呼び出します。 これにより、サービスに固有のタスクを実行するサービスです。 
    
2. メッセージ サービスを削除します。
    
3. メッセージ サービスのプロファイル セクションを削除します。
    
サービスが削除された後、メッセージ サービスのエントリ ポイント関数は再び呼び出されません。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージ サービスを削除するのには、 **MAPIUID**構造体を取得するには、メッセージ サービスのテーブルの行のメッセージ サービスから**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) のプロパティの列を取得します。 詳細については、 [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)メソッドで説明する手順を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDeleteSelectedItem  <br/> |MFCMAPI では、 **IMsgServiceAdmin::DeleteMsgService**メソッドを使用して、選択したサービスを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

