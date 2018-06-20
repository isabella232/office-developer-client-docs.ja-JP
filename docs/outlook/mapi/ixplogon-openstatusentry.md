---
title: IXPLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 261d5f7c-bb61-4e1d-aa41-cca224c63f8e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0e96c0b99f0a5f7511ed59b483ab9409eafad882
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801249"
---
# <a name="ixplogonopenstatusentry"></a>IXPLogon::OpenStatusEntry

  
  
**適用されます**: Outlook 
  
トランスポート プロバイダーの状態のオブジェクトを開きます。
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> [in]トランスポート ログオン オブジェクトのインターフェイス id (IID) へのポインター。 [IMAPIStatus](imapistatusimapiprop.md)インターフェイスを返します NULL を渡すことです。 _LpInterface_パラメーターは、オブジェクトのインターフェイスの識別子を設定することも。 
    
 _ulFlags_
  
> [in]状態オブジェクトを開く方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_MODIFY 
  
> 要求の読み取り/書き込みのアクセス許可 デフォルトのインタ フェースは、読み取り専用です。 
    
 _lpulObjType_
  
> [out]開かれたオブジェクトの型へのポインター。
    
 _lppEntry_
  
> [out]開かれた状態のオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
## <a name="remarks"></a>備考

MAPI スプーラーは、クライアント アプリケーションは、トランスポート プロバイダーの状態のテーブルの行のエントリ id の**OpenEntry**メソッドを呼び出すときに、 **IXPLogon::OpenStatusEntry**メソッドを呼び出します。 **OpenStatusEntry**は、この特定のトランスポート プロバイダーへのログオンに関連付けられている**IMAPIStatus**インターフェイスを持つオブジェクトを開きます。 (たとえば、 [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)メソッドを使用してログオン セッションを再構成するか、[を使用してログオン セッションの状態を検証するために**IMAPIStatus**メソッドを呼び出すクライアント アプリケーションを有効にするのにはこのオブジェクトを使用してIMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッド)。 
  
## <a name="see-also"></a>関連項目



[IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon: IUnknown](ixplogoniunknown.md)

