---
title: IMAPIOfflineMgrUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 800f79179f999ba193d4177abb7341095b8b896d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404856"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オフラインオブジェクトのコールバックをキャンセルします。
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番コールバックをキャンセルするためのフラグ。 MAPIOFFLINE_UNADVISE_DEFAULT の値のみがサポートされています。
    
 _ulAdviseToken_
  
> 順番キャンセルされるコールバック登録を識別するアドバイズトークン。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> 呼び出しが正常になされました。 この呼び出しは S_OK を返す必要があります。
    
## <a name="remarks"></a>注釈

以前の**[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)** への呼び出しから返された*ulAdviseToken*に関連付けられていたコールバックの登録を削除します。 **IMAPIOfflineMgr**オブジェクトは、 *ulAdviseToken*に関連付けられた**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** オブジェクトに対する参照を解放します。 
  
## <a name="see-also"></a>関連項目



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[MAPI 定数](mapi-constants.md)

