---
title: IProfAdminDeleteProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.DeleteProfile
api_type:
- COM
ms.assetid: 730af2da-4c4a-42a7-9d52-56d914107d64
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 249d2dcf3a298abde85bdc53620680146d43c168
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801144"
---
# <a name="iprofadmindeleteprofile"></a>IProfAdmin::DeleteProfile

  
  
**適用されます**: Outlook 
  
プロファイルを削除します。
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpszProfileName_
  
> [in]削除するプロファイルの名前へのポインター。
    
 _ulFlags_
  
> [in]常に NULL を返します。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロファイルが正常に削除されました。
    
MAPI_E_NOT_FOUND 
  
> 指定されたプロファイルが存在しません。
    
## <a name="remarks"></a>備考

**IProfAdmin::DeleteProfile**メソッドは、プロファイルを削除します。 **DeleteProfile**が呼び出されたときに削除するプロファイルを使用している場合、 **DeleteProfile**は S_OK を返しますが、すぐに、プロファイルは削除されません。 代わりに、 **DeleteProfile**は、プロファイルの削除をマークし、不要になった使用されている、すべてのアクティブ ・ セッションの終了したときに後でそれを削除します。 
  
プロファイルでは、各メッセージ サービスのエントリ ポイント関数は、 _ulContext_パラメーターに設定された MSG_SERVICE_DELETE 値で呼び出されます。 関数は、サービスを削除し、サービスのプロファイル セクションを削除し、最初に、します。 サービスが削除された後、メッセージ サービスのエントリ ポイント関数は再び呼び出されません。 
  
パスワードがプロファイルを削除する必要はありません。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrRemoveProfile  <br/> |MFCMAPI では、 **IProfAdmin::DeleteProfile**メソッドを使用して、選択したプロファイルを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin: IUnknown](iprofadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

