---
title: IMsgServiceAdminDeleteMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.DeleteMsgService
api_type:
- COM
ms.assetid: 3a6b34eb-9d46-488f-8d02-91b27c35de67
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 053ead29442c847a0b5a786263845a1dc8a6c6ef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556428"
---
# <a name="imsgserviceadmindeletemsgservice"></a>IMsgServiceAdmin::DeleteMsgService

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルからメッセージ サービスを削除します。
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a>パラメーター

 _lpuid_
  
> [in]削除するメッセージ サービスの一意の識別子を含む [MAPIUID](mapiuid.md) 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージ サービスが削除されました。
    
MAPI_E_NOT_FOUND 
  
> **lpuid が** 指す _MAPIUID_ は、既存のメッセージ サービスと一致しません。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin::D eleteMsgService** メソッドは、プロファイルからメッセージ サービスを削除します。 **DeleteMsgService** は、メッセージ サービスに関連するすべてのプロファイル セクションを削除します。 
  
 **DeleteMsgService は** 、次の手順を実行してメッセージ サービスを削除します。 
  
1. プロファイル セクションが削除される前に  _、ulContext_ パラメーターが MSG_SERVICE_DELETEメッセージ サービスのエントリ ポイント関数を呼び出します。 これにより、サービスはサービス固有のタスクを実行できます。 
    
2. メッセージ サービスを削除します。
    
3. メッセージ サービスのプロファイル セクションを削除します。
    
メッセージ サービスのエントリ ポイント関数は、サービスが削除された後に再度呼び出されません。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

削除するメッセージ サービスの **MAPIUID** 構造を取得するには、メッセージ サービス テーブルのメッセージ サービスの行から **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティ列を取得します。 詳細については [、「IMsgServiceAdmin::CreateMsgService メソッド」で説明されている手順を参照](imsgserviceadmin-createmsgservice.md) してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDeleteSelectedItem  <br/> |MFCMAPI は **、IMsgServiceAdmin::D eleteMsgService** メソッドを使用して、選択したサービスを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

