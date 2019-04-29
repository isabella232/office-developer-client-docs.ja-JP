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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f50c0eb9e3af68e206eaa5bcc51cefa923c30f72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413179"
---
# <a name="imslogonopenstatusentry"></a>IMSLogon::OpenStatusEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
status オブジェクトを開きます。
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a>パラメーター

 _lpinterface_
  
> 順番開く状態オブジェクトのインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、オブジェクトの標準インターフェイスが返されます (この場合は[imapistatus](imapistatusimapiprop.md)インターフェイス)。 _lpinterface_パラメーターは、オブジェクトの適切なインターフェイスの識別子に設定することもできます。 
    
 _ulFlags_
  
> 順番status オブジェクトが開かれる方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用のアクセス許可で作成され、読み取り/書き込みアクセス許可が与えられているという前提でクライアントアプリケーションを使用することはできません。 
    
 _lpulobjtype_
  
> 読み上げ開かれているオブジェクトの種類へのポインター。
    
 _lppentry_
  
> 読み上げ開かれているオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

メッセージストアプロバイダーは、status オブジェクトを開くために**IMSLogon:: openstatusentry**メソッドを実装します。 この状態オブジェクトは、クライアントが[imapistatus](imapistatusimapiprop.md)メソッドを呼び出せるようにするために使用されます。 たとえば、クライアントは[imapistatus:: settingsdialog](imapistatus-settingsdialog.md)メソッドを使用して、メッセージストアログオンセッションまたは[imapistatus:: validatestate](imapistatus-validatestate.md)メソッドを再構成し、メッセージストアログオンセッションの状態を検証することができます。 
  
## <a name="see-also"></a>関連項目



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

