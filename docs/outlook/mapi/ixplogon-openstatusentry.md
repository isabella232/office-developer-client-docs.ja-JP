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
  
トランスポート プロバイダーの状態オブジェクトを開きます。
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a>パラメーター

 _lpInterface_
  
> [in]トランスポート ログオン オブジェクトのインターフェイス識別子 (IID) へのポインター。 NULL を渡すと [、IMAPIStatus インターフェイスが返](imapistatusimapiprop.md) されます。 _lpInterface パラメーター_ は、オブジェクトのインターフェイスの識別子に設定することもできます。 
    
 _ulFlags_
  
> [in]status オブジェクトの開き方を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定のインターフェイスは読み取り専用です。 
    
 _lpulObjType_
  
> [out]開いたオブジェクトの種類へのポインター。
    
 _lppEntry_
  
> [out]開いた状態オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値または値を返しました。
    
## <a name="remarks"></a>注釈

MAPI スプーラーは、クライアント アプリケーションがトランスポート プロバイダーの状態テーブル行のエントリ識別子の **OpenEntry** メソッドを呼び出す場合に **、IXPLogon::OpenStatusEntry** メソッドを呼び出します。 **OpenStatusEntry は、** この特定のトランスポート プロバイダーログオンに関連付けられた **IMAPIStatus** インターフェイスを持つオブジェクトを開きます。 次に、このオブジェクトを使用して、クライアント アプリケーションが **IMAPIStatus** メソッドを呼び出す (たとえば [、IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) メソッドを使用してログオン セッションを再構成したり [、IMAPIStatus::ValidateState](imapistatus-validatestate.md) メソッドを使用してログオン セッションの状態を検証したりするために使用されます)。 
  
## <a name="see-also"></a>関連項目



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

