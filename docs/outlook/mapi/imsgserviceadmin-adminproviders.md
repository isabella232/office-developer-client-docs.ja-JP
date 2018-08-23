---
title: IMsgServiceAdminAdminProviders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.AdminProviders
api_type:
- COM
ms.assetid: 0d605e2c-10db-46e1-95d5-12fabd524baa
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1b03245d7af4c6fb3879e597d8345e5d9888e164
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567210"
---
# <a name="imsgserviceadminadminproviders"></a>IMsgServiceAdmin::AdminProviders

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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
  
> [in]管理するメッセージ サービスの一意の識別子を格納する[MAPIUID](mapiuid.md)構造体へのポインター。 
    
 _ulFlags_
  
> [in]常に NULL を返します。 
    
 _lppProviderAdmin_
  
> [out]プロバイダーの管理オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロバイダーの管理オブジェクトが正常に返されました。
    
MAPI_E_NOT_FOUND 
  
> _LpUID_で示される**MAPIUID**は存在しません。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin::AdminProviders**メソッドは、プロバイダーの管理オブジェクトへのアクセスを提供します。 プロバイダーの管理は、 [IProviderAdmin](iprovideradminiunknown.md)インターフェイスをサポートしていて、クライアントは、次の操作を可能にするオブジェクトです。 
  
- メッセージ サービスにサービス プロバイダーを追加します。
    
- メッセージ サービスからサービス プロバイダーを削除します。
    
- プロファイル セクションを開きます。
    
- メッセージ サービス プロバイダー テーブルにアクセスします。
    
実際に可能なメッセージ サービスにプロファイルを使用中に変更の種類は、メッセージ サービスに依存します。 ただし、ほとんどのメッセージ サービスには、追加し、プロファイルを使用している間に、プロバイダーを削除するなどの変更はできません。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージ サービスを管理するための**MAPIUID**構造体を取得するには、メッセージ サービスのテーブルの行のメッセージ サービスから**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) のプロパティの列を取得します。 詳細については、 [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)メソッドで説明する手順を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI では、 **IMsgServiceAdmin::AdminProviders**メソッドを使用して、サービス プロバイダーの管理オブジェクトを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IProviderAdmin : IUnknown](iprovideradminiunknown.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

