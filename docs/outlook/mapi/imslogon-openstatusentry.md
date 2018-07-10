---
title: IMSLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 850e256b-6b50-428c-aede-287edaf7b005
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 55cf41d251db4c84dad9f12d8f83d0b0dda63ff3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801043"
---
# <a name="imslogonopenstatusentry"></a>IMSLogon::OpenStatusEntry

  
  
**適用されます**: Outlook 
  
状態オブジェクトを開きます。
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> [in]開くには、状態オブジェクトのインターフェイス id (IID) へのポインター。 NULL を渡すことを示します (ここでは、 [IMAPIStatus](imapistatusimapiprop.md)インターフェイス) オブジェクトの標準的なインターフェイスが返されます。 _LpInterface_パラメーターは、オブジェクトの適切なインターフェイスの識別子を設定することも。 
    
 _ulFlags_
  
> [in]状態オブジェクトを開く方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_MODIFY 
  
> 要求の読み取り/書き込みのアクセス許可 既定では、読み取り専用の権限を持つオブジェクトが作成およびクライアント アプリケーションは読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。 
    
 _lpulObjType_
  
> [out]開かれたオブジェクトの型へのポインター。
    
 _lppEntry_
  
> [out]開かれたオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

メッセージ ストア プロバイダーは、状態オブジェクトを開くには、 **IMSLogon::OpenStatusEntry**メソッドを実装します。 [IMAPIStatus](imapistatusimapiprop.md)メソッドを呼び出すクライアントを有効にするこの状態のオブジェクトを使用しています。 たとえば、クライアントは、メッセージ ストアのログオン セッションまたはメッセージ ストアのログオン セッションの状態を検証するために[IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドを再構成するのには、 [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)メソッドを使用できます。 
  
## <a name="see-also"></a>関連項目



[IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon: IUnknown](imslogoniunknown.md)
