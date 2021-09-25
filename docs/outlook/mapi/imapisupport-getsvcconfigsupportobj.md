---
title: IMAPISupportGetSvcConfigSupportObj
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.GetSvcConfigSupportObj
api_type:
- COM
ms.assetid: 56c3bdae-a3a8-4334-b6d2-a89c6820d72e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a7ed092639c7a0e7a6c1b1d39c01006ec87fdb85
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567446"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a>IMAPISupport::GetSvcConfigSupportObj

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ サービスサポート オブジェクトを作成します。
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lppSvcSupport_
  
> [out]新しいメッセージ サービス サポート オブジェクトへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 構成サポート オブジェクトが正常に作成されました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::GetSvcConfigSupportObj** メソッドは、すべてのサポート オブジェクトに実装されます。 サービス プロバイダーは **GetSvcConfigSupportObj** を呼び出して、メッセージ サービス エントリ ポイント関数に渡す構成サポート オブジェクトを作成します。 
  
メッセージ サービスエントリ ポイント関数は [、MSGSERVICEENTRY](msgserviceentry.md) プロトタイプに基づいており [、IMsgServiceAdmin インターフェイスのメソッドによって呼び出](imsgserviceadminiunknown.md) されます。 メッセージ サービス エントリ ポイント関数を使用すると、プロファイルが変更された場合に、メッセージ サービスが自分自身を構成したり、他のアクションを実行したりできます。 メッセージ サービスエントリ ポイント関数は、プロパティ シートを表示するか [、IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) メソッドに渡されるプロパティ値配列を介して構成の変更をサポートできます。 
  
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

