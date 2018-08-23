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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: aa3c010eafeba7908498965bc0491c993a4a9120
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572088"
---
# <a name="iprofadmindeleteprofile"></a>IProfAdmin::DeleteProfile

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロファイルを削除します。
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpszProfileName_
  
> [in]削除するプロファイルの名前へのポインター。
    
 _ulFlags_
  
> [in]常に NULL を返します。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロファイルが正常に削除されました。
    
MAPI_E_NOT_FOUND 
  
> 指定されたプロファイルが存在しません。
    
## <a name="remarks"></a>注釈

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
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

