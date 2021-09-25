---
title: IMAPISupportSetProviderUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 270e1486c7c33ea8655914bf9fe51e9f335fc707
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575744"
---
# <a name="imapisupportsetprovideruid"></a>IMAPISupport::SetProviderUID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービス プロバイダーを [一意に表す MAPIUID](mapiuid.md) 構造体を登録します。 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpProviderID_
  
> [in]アドレス帳またはメッセージ ストア プロバイダーを識別する **MAPIUID** 構造体へのポインター。 
    
 _ulFlags_
  
> 予約済み。は 0 である必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> **MAPIUID 構造** が正常に登録されました。 
    
## <a name="remarks"></a>注釈

**IMAPISupport::SetProviderUID** メソッドは、アドレス帳およびメッセージ ストア プロバイダーのサポート オブジェクトに実装されます。 これらのプロバイダーは **SetProviderUID** を呼び出して _、lpProviderID_ によって指される **MAPIUID** 構造で説明されている一意の識別子を登録します。 プロバイダーは、この識別子を作成するエントリ識別子のすべてに含まれます。 
  
MAPI は **、MAPI スプーラー** に送信メッセージを送信するときに MAPIUID 構造を使用し、クライアント要求を処理する適切なプロバイダーを決定します。 たとえば、クライアントが [IMAPISession::OpenEntry](imapisession-openentry.md) メソッドを呼び出す場合、MAPI はエントリ識別子の **MAPIUID** 部分を調べ、それを **SetProviderUID** に渡したプロバイダーにマップし、そのプロバイダーの **OpenEntry** を呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**ログオン時に SetProviderUID** を呼び出して **、MAPIUID 構造を登録** します。 MAPI を使用すると、アドレス帳とメッセージ ストア プロバイダーは複数の識別子を登録できます。 **SetProviderUID** を複数呼び出す場合は **、MAPIUID** が重複している場合でも、常に **MAPIUID** 構造体をプロバイダーの MAPIUID 構造体のセットに追加します。 **SetProviderUID は** **MAPIUID を削除できません**。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

