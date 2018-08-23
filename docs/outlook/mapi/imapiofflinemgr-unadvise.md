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
ms.openlocfilehash: 35dfc7af9852609dcfcc3fcb9d65ec2e4afa9632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579523"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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
    
## <a name="remarks"></a>注釈

*UlAdviseToken* **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** 前回の呼び出しから返されると、関連付けられているコールバックの登録を削除します。 *UlAdviseToken*に関連付けられている**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** オブジェクトの参照を解放する**IMAPIOfflineMgr**オブジェクトが発生します。 
  
## <a name="see-also"></a>関連項目



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[MAPI �萔](mapi-constants.md)

