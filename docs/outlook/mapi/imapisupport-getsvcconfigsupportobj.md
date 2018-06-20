---
title: IMAPISupportGetSvcConfigSupportObj
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetSvcConfigSupportObj
api_type:
- COM
ms.assetid: 56c3bdae-a3a8-4334-b6d2-a89c6820d72e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5d7e3e89f15b1bc08c7ce9faab0d0a6326300e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800740"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a>IMAPISupport::GetSvcConfigSupportObj

  
  
**適用されます**: Outlook 
  
メッセージ サービスのサポート オブジェクトを作成します。
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lppSvcSupport_
  
> [out]メッセージ サービスのサポートの新しいオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 構成のサポート オブジェクトが正常に作成されました。
    
## <a name="remarks"></a>備考

サポートのすべてのオブジェクトの**IMAPISupport::GetSvcConfigSupportObj**メソッドを実装します。 サービス プロバイダーは、メッセージ サービスのエントリ ポイント関数に渡す設定のサポート オブジェクトを作成するのには**GetSvcConfigSupportObj**を呼び出します。 
  
メッセージ サービスのエントリ ポイント関数では、 [MSGSERVICEENTRY](msgserviceentry.md)のプロトタイプに基づいており、 [IMsgServiceAdmin](imsgserviceadminiunknown.md)インターフェイスのメソッドによって呼び出されます。 メッセージ サービスのエントリ ポイント関数は、メッセージ サービス自体を構成するか、プロファイルが変更されたときに、その他のアクションを実行できます。 メッセージ サービスのエントリ ポイント関数は、プロパティ シートを表示することによって、またはプロパティ値の配列を構成の変更をサポートできますが、 [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)メソッドに渡されます。 
  
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md)
  
[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[IProfAdmin: IUnknown](iprofadminiunknown.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

