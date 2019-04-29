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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d9e09de1064a0ae034bb3618f0e5b3719a82c163
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435902"
---
# <a name="ixplogonopenstatusentry"></a>IXPLogon::OpenStatusEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポートプロバイダーの状態オブジェクトを開きます。
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a>パラメーター

 _lpinterface_
  
> 順番トランスポートログオンオブジェクトのインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、 [imapistatus](imapistatusimapiprop.md)インターフェイスが返されます。 _lpinterface_パラメーターは、オブジェクトのインターフェイスの識別子に設定することもできます。 
    
 _ulFlags_
  
> 順番status オブジェクトが開かれる方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定のインターフェイスは読み取り専用です。 
    
 _lpulobjtype_
  
> 読み上げ開かれているオブジェクトの種類へのポインター。
    
 _lppentry_
  
> 読み上げ開かれた状態オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、予想される値または値が返されました。
    
## <a name="remarks"></a>注釈

クライアントアプリケーションがトランスポートプロバイダーの状態テーブルの行のエントリ id に対して**openentry**メソッドを呼び出すと、MAPI スプーラーは**IXPLogon:: openstatusentry**メソッドを呼び出します。 **openstatusentry**この特定のトランスポートプロバイダーログオンに関連付けられている**imapistatus**インターフェイスを持つオブジェクトを開きます。 次に、このオブジェクトを使用して、クライアントアプリケーションが**imapistatus**メソッドを呼び出すことができるようにします (たとえば、 [imapistatus:: settingsdialog](imapistatus-settingsdialog.md)メソッドを使用してログオンセッションを再構成する場合、またはを使用[してログオンセッションの状態を確認する場合など)。imapistatus:: validatestate](imapistatus-validatestate.md)メソッド)。 
  
## <a name="see-also"></a>関連項目



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

