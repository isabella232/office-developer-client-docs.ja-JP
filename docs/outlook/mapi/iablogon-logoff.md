---
title: IABLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e441e84e0bddff2e5a989849dbcf593320340d2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800350"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**適用されます**: Outlook 
  
ログオフ処理を開始します。
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> ログオフ処理が正常に開始されました。
    
## <a name="remarks"></a>備考

ログオフ処理は通常、クライアントがセッションを終了するのには[IMAPISession::Logoff](imapisession-logoff.md)メソッドを呼び出すときに起動します。 MAPI は、ログオフ処理を開始するのには、各アドレス帳プロバイダーの**IABLogon::Logoff**メソッドを呼び出します。 
  
**IABLogon::Logoff**メソッドは、次のこと。 
  
- サブオブジェクトまたは状態オブジェクトなど、すべての開いているオブジェクトを解放します。
    
- プロバイダーのサポートのオブジェクトを解放します。
    
アドレス帳プロバイダーのログオフ処理の詳細については、[シャット ダウン、サービス ・ プロバイダー](shutting-down-a-service-provider.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon: IUnknown](iablogoniunknown.md)

