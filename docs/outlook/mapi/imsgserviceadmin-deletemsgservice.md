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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6cef03e33abab81a407698b73a007f247ef88194
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407383"
---
# <a name="imsgserviceadmindeletemsgservice"></a>IMsgServiceAdmin::DeleteMsgService

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージサービスをプロファイルから削除します。
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a>パラメーター

 _lpuid_
  
> 順番削除するメッセージサービスの一意の識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージサービスが削除されました。
    
MAPI_E_NOT_FOUND 
  
> _lpuid_が指す**MAPIUID**が、既存のメッセージサービスと一致しません。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin::D eletemsgservice**メソッドは、プロファイルからメッセージサービスを削除します。 **DeleteMsgService**は、メッセージサービスに関連するすべてのプロファイルセクションを削除します。 
  
 **DeleteMsgService**は、次の手順を実行して、メッセージサービスを削除します。 
  
1. _ulcontext_パラメーターを MSG_SERVICE_DELETE に設定してメッセージサービスのエントリポイント関数を呼び出して、プロファイルセクションが削除されるようにします。 これにより、サービスはサービス固有のタスクを実行できるようになります。 
    
2. メッセージサービスを削除します。
    
3. メッセージサービスのプロファイルセクションを削除します。
    
サービスが削除された後、メッセージサービスのエントリポイント関数が再度呼び出されることはありません。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

削除するメッセージサービスの**MAPIUID**構造を取得するには、メッセージサービステーブルのメッセージサービスの行から**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティ列を取得します。 詳細については、 [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md)メソッドに記載されている手順を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgServiceTableDlg  <br/> |CMsgServiceTableDlg:: OnDeleteSelectedItem  <br/> |mfcmapi は、 **IMsgServiceAdmin::D eletemsgservice**メソッドを使用して、選択されているサービスを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

