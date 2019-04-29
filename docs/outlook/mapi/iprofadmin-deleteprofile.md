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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8aafb849a98028efb37646752a7b49fa5e6ef2ff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419591"
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

 _lpszprofilename_
  
> 順番削除するプロファイルの名前へのポインター。
    
 _ulFlags_
  
> 順番常に NULL。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロファイルが正常に削除されました。
    
MAPI_E_NOT_FOUND 
  
> 指定されたプロファイルが存在しません。
    
## <a name="remarks"></a>注釈

**IProfAdmin::D eleteprofile**メソッドは、プロファイルを削除します。 **deleteprofile**を呼び出したときに削除するプロファイルが使用されている場合、 **deleteprofile**は S_OK を返しますが、プロファイルはすぐには削除されません。 代わりに、 **deleteprofile**はプロファイルを削除対象としてマークし、使用されなくなった後に、すべてのアクティブなセッションが終了した時点で削除します。 
  
プロファイル内の各メッセージサービスのエントリポイント関数は、 _ulcontext_パラメーターで設定された MSG_SERVICE_DELETE 値を使用して呼び出されます。 最初に、この関数はサービスを削除してから、サービスの [プロファイル] セクションを削除します。 サービスが削除された後に、メッセージサービスエントリポイント関数が再度呼び出されることはありません。 
  
プロファイルを削除するためにパスワードは必要ありません。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProfileFunctions  <br/> |hrremoveprofile  <br/> |mfcmapi は、 **IProfAdmin::D eleteprofile**メソッドを使用して、選択されているプロファイルを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

