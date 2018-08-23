---
title: IOSTXSyncHdrBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrBeg
api_type:
- COM
ms.assetid: 7f8ca7cf-ac0b-9b77-c1dd-9f1d0871d603
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a5c754a209a3e1bce8888851b88e116f92920eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801088"
---
# <a name="iostxsynchdrbeg"></a>IOSTX::SyncHdrBeg

  
  
**適用対象**: Outlook 
  
メッセージ ヘッダーの同期を開始します。
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>パラメーター

 _cbeid_
  
> [in]メッセージのエントリ ID 内のバイト数です。
    
 _lpeid_
  
> [in]メッセージのエントリ ID です。
    
 _ppv_
  
>  [内] と [出力] メッセージ ヘッダーの**[HDRSYNC](hdrsync.md)** 構造体へのポインター。 
    
## <a name="remarks"></a>注釈

**IOSTX::SyncHdrBeg**、時に、ローカルは、[メッセージ ヘッダーの状態をダウンロードする](download-message-header-state.md)に効果を格納します。 Outlook は、クライアントがストアに格納され、親フォルダーのメッセージのヘッダーの現在の表現を**HDRSYNC**構造体を初期化します。 クライアントは、( *pmsgFull*の**HDRSYNC**で) として、完全なメッセージ項目をダウンロードする必要があります。 これが成功した場合、クライアントも*ulFlags*の設定**HDRSYNC** **HSF_OK**とします。 **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**、時に、Outlook は**HDRSYNC**の結果をチェックし、 **HDRSYNC**で情報を使用して、ローカルのメッセージ ヘッダーを更新します。 
  
## <a name="see-also"></a>関連項目



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI �萔](mapi-constants.md)

