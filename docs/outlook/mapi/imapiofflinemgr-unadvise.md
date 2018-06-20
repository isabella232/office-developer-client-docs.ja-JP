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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b52dcd87c8714ad59db560a5ae4a8300f9cc83ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800631"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**適用されます**: Outlook 
  
オフライン オブジェクトのコールバックをキャンセルします。
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]コールバックをキャンセルするためのフラグです。 MAPIOFFLINE_UNADVISE_DEFAULT の値のみがサポートされています。
    
 _ulAdviseToken_
  
> [in]アドバイズを識別するトークンをキャンセルするのには、コールバックが登録します。 
    
## <a name="return-value"></a>�߂�l

S_OK
  
> 呼び出しが正常になされました。 この呼び出しでは、S_OK を返す必要があります。
    
## <a name="remarks"></a>備考

*UlAdviseToken* **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** 前回の呼び出しから返されると、関連付けられているコールバックの登録を削除します。 *UlAdviseToken*に関連付けられている**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** オブジェクトの参照を解放する**IMAPIOfflineMgr**オブジェクトが発生します。 
  
## <a name="see-also"></a>関連項目



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[MAPI �萔](mapi-constants.md)

