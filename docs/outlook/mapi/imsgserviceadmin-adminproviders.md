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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6b7360995a781824b50ff02b5d2dec8e481e7ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422762"
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

 _lpuid_
  
> 順番管理するメッセージサービスの一意の識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。 
    
 _ulFlags_
  
> 順番常に NULL。 
    
 _lppprovideradmin_
  
> 読み上げプロバイダー管理オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロバイダー管理オブジェクトが正常に返されました。
    
MAPI_E_NOT_FOUND 
  
> _lpuid_が指す**MAPIUID**が存在しません。 
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin:: adminproviders**メソッドは、プロバイダ管理オブジェクトへのアクセスを提供します。 プロバイダー管理は、 [IProviderAdmin](iprovideradminiunknown.md)インターフェイスをサポートし、クライアントが次の操作を実行できるようにするオブジェクトです。 
  
- メッセージサービスにサービスプロバイダーを追加します。
    
- メッセージサービスからサービスプロバイダーを削除します。
    
- [プロファイル] セクションを開きます。
    
- メッセージサービスプロバイダテーブルにアクセスします。
    
プロファイルが使用されている間にメッセージサービスに対して実際に行うことができる変更の種類は、メッセージサービスによって異なります。 ただし、ほとんどのメッセージサービスでは、プロファイルの使用中にプロバイダーを追加および削除するなどの変更はサポートされていません。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

管理するメッセージサービスの**MAPIUID**構造を取得するには、メッセージサービステーブルのメッセージサービスの行から**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティ列を取得します。 詳細については、 [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md)メソッドに記載されている手順を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgServiceTableDlg  <br/> |CMsgServiceTableDlg:: ondisplayitem  <br/> |mfcmapi は、 **IMsgServiceAdmin:: adminproviders**メソッドを使用して、サービスのプロバイダー管理オブジェクトを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IProviderAdmin : IUnknown](iprovideradminiunknown.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

