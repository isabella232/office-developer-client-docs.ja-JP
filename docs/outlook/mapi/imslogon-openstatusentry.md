---
title: IMSLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 850e256b-6b50-428c-aede-287edaf7b005
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: acb42aa4fedf0cdd006553cbeb9a5a5be96f61b1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620675"
---
# <a name="imslogonopenstatusentry"></a>IMSLogon::OpenStatusEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
状態オブジェクトを開きます。
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a>パラメーター

 _lpInterface_
  
> [in]status オブジェクトを開くインターフェイス識別子 (IID) へのポインター。 NULL を渡す場合は、オブジェクトの標準インターフェイスが返されます (この場合は [IMAPIStatus](imapistatusimapiprop.md) インターフェイス)。 _lpInterface パラメーター_ は、オブジェクトの適切なインターフェイスの識別子に設定することもできます。 
    
 _ulFlags_
  
> [in]status オブジェクトの開き方を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用のアクセス許可で作成され、クライアント アプリケーションは、読み取り/書き込みアクセス許可が付与されているという前提で動作しません。 
    
 _lpulObjType_
  
> [out]開いたオブジェクトの種類へのポインター。
    
 _lppEntry_
  
> [out]開いたオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

メッセージ ストア プロバイダーは、状態オブジェクトを開く **IMSLogon::OpenStatusEntry** メソッドを実装します。 この状態オブジェクトは、クライアントが [IMAPIStatus メソッドを呼び出すのを有効に](imapistatusimapiprop.md) するために使用されます。 たとえば、クライアントは [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) メソッドを使用してメッセージ ストア ログオン セッションを再構成したり [、IMAPIStatus::ValidateState](imapistatus-validatestate.md) メソッドを使用してメッセージ ストア ログオン セッションの状態を検証できます。 
  
## <a name="see-also"></a>関連項目



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

