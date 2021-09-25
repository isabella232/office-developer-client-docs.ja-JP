---
title: IProfAdminDeleteProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.DeleteProfile
api_type:
- COM
ms.assetid: 730af2da-4c4a-42a7-9d52-56d914107d64
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 83bae85596603dc5ef2700cd008b2b44e2fde08a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587882"
---
# <a name="iprofadmindeleteprofile"></a>IProfAdmin::DeleteProfile

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
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
  
> [in]常に NULL。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロファイルが正常に削除されました。
    
MAPI_E_NOT_FOUND 
  
> 指定したプロファイルが存在しません。
    
## <a name="remarks"></a>注釈

**IProfAdmin::D eleteProfile** メソッドはプロファイルを削除します。 DeleteProfile の呼び出し時に削除するプロファイルが使用されている場合 **、DeleteProfile** は S_OKを返しますが、プロファイルはすぐには削除されません。  代わりに **、DeleteProfile は** プロファイルに削除のマークを付け、すべてのアクティブ なセッションが終了すると、使用されなくなった後にプロファイルを削除します。 
  
プロファイル内の各メッセージ サービスのエントリ ポイント関数は、ulContext パラメーターに設定MSG_SERVICE_DELETEを使用して  _呼び出_ されます。 最初に、関数はサービスを削除し、次にサービスのプロファイル セクションを削除します。 サービスが削除された後、メッセージ サービスエントリ ポイント関数は再度呼び出されません。 
  
プロファイルを削除するには、パスワードは必要ありません。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrRemoveProfile  <br/> |MFCMAPI は **、IProfAdmin::D eleteProfile** メソッドを使用して、選択したプロファイルを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

