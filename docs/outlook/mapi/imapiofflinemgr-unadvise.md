---
title: IMAPIOfflineMgrUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 29d6b7bf1e8bbb9d9fb1d5a17441fb779d9d67ef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604867"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オフライン オブジェクトのコールバックをキャンセルします。
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]コールバックをキャンセルするフラグ。 サポートされているMAPIOFFLINE_UNADVISE_DEFAULT値のみです。
    
 _ulAdviseToken_
  
> [in]取り消すコールバック登録を識別するアドバイス トークン。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> 呼び出しが正常になされました。 この呼び出しは、S_OK。
    
## <a name="remarks"></a>注釈

**[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** への以前の呼び出しから返された *ulAdviseToken* に関連付けられたコールバックの登録を削除します。 *ULAdviseToken* に関連付けられた **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** オブジェクト上の **IMAPIOfflineMgr** オブジェクトの参照を解放します。 
  
## <a name="see-also"></a>関連項目



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[MAPI 定数](mapi-constants.md)

