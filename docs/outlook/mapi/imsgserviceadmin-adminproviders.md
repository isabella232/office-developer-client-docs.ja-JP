---
title: IMsgServiceAdminAdminProviders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.AdminProviders
api_type:
- COM
ms.assetid: 0d605e2c-10db-46e1-95d5-12fabd524baa
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 733ec8ec6e24e165e0cc30dadd67b2bebdb6b00c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571697"
---
# <a name="imsgserviceadminadminproviders"></a>IMsgServiceAdmin::AdminProviders

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダー管理オブジェクトへのアクセスを提供するポインターを返します。
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a>パラメーター

 _lpUID_
  
> [in]管理するメッセージ サービスの一意の識別子を含む [MAPIUID](mapiuid.md) 構造体へのポインター。 
    
 _ulFlags_
  
> [in]常に NULL。 
    
 _lppProviderAdmin_
  
> [out]プロバイダー管理オブジェクトへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロバイダー管理オブジェクトが正常に返されました。
    
MAPI_E_NOT_FOUND 
  
> **lpUID が** 指す _MAPIUID_ が存在しません。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin::AdminProviders メソッドは**、プロバイダー管理オブジェクトへのアクセスを提供します。 プロバイダー管理は [、IProviderAdmin](iprovideradminiunknown.md) インターフェイスをサポートし、クライアントが次の操作を実行できるオブジェクトです。 
  
- サービス プロバイダーをメッセージ サービスに追加します。
    
- メッセージ サービスからサービス プロバイダーを削除します。
    
- プロファイル セクションを開きます。
    
- メッセージ サービス プロバイダー テーブルにアクセスします。
    
プロファイルの実行中に実際にメッセージ サービスに対して行える変更の種類は、メッセージ サービスによって異なります。 ただし、ほとんどのメッセージ サービスでは、プロファイルの実行中にプロバイダーの追加や削除などの変更はサポートされていません。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

管理するメッセージ サービスの **MAPIUID** 構造を取得するには、メッセージ サービス テーブルのメッセージ サービスの行から **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティ列を取得します。 詳細については [、「IMsgServiceAdmin::CreateMsgService メソッド」で説明されている手順を参照](imsgserviceadmin-createmsgservice.md) してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI は **、IMsgServiceAdmin::AdminProviders** メソッドを使用して、サービスのプロバイダー管理オブジェクトを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IProviderAdmin : IUnknown](iprovideradminiunknown.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

