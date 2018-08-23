---
title: IMAPISupportSetProviderUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2182ec71c54c81e9a43a34973e005292ddccdfff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800792"
---
# <a name="imapisupportsetprovideruid"></a>IMAPISupport::SetProviderUID

  
  
**適用対象**: Outlook 
  
サービス プロバイダーを一意に表す[MAPIUID](mapiuid.md)構造体を登録します。 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpProviderID_
  
> [in]アドレス帳またはメッセージ ストア プロバイダーを識別する**MAPIUID**構造体へのポインター。 
    
 _ulFlags_
  
> 予約されています。0 にする必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> **MAPIUID**構造体は正常に登録されました。 
    
## <a name="remarks"></a>注釈

アドレス帳、メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::SetProviderUID**メソッドを実装します。 これらのプロバイダーは、 _lpProviderID_に設定されている**MAPIUID**構造体で記載されている一意の識別子を登録するのには**SetProviderUID**を呼び出します。 プロバイダーには、すべてのエントリの識別子を作成するのにこの識別子が含まれます。 
  
MAPI は、MAPI スプーラーを無効にし、クライアントの要求を処理するための適切なプロバイダーを確認するのには送信メッセージを送信するときに、 **MAPIUID**構造体を使用します。 たとえば、クライアントは、 [IMAPISession::OpenEntry](imapisession-openentry.md)メソッドを呼び出すと、MAPI、 **MAPIUID**の部分のエントリ id を調べ、 **SetProviderUID**に渡されることと、そのプロバイダーの**OpenEntry**を呼び出すためのプロバイダーにマップ. 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**MAPIUID**構造体を登録するのにはログオン時に**SetProviderUID**を呼び出します。 MAPI では、複数の識別子を登録するのには、アドレス帳、メッセージ ストア プロバイダーを使用できます。 **SetProviderUID**に複数の呼び出しの際に、常に**MAPIUID**構造体に追加プロバイダーのセットを**MAPIUID**構造体の**MAPIUID**は、重複している場合でも。 **SetProviderUID**は、 **MAPIUID**を削除できません。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

