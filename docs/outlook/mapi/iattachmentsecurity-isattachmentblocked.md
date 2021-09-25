---
title: IAttachmentSecurityIsAttachmentBlocked
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAttachmentSecurity.IsAttachmentBlocked
api_type:
- COM
ms.assetid: 6986d27a-9602-e44a-0797-4c47f2184ef7
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 80fdb13233b4ad345c3cbef62a733df2f130d527
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580035"
---
# <a name="iattachmentsecurityisattachmentblocked"></a>IAttachmentSecurity::IsAttachmentBlocked

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定した添付ファイルが、表示およびインデックス作成Microsoft Outlook 2010またはMicrosoft Outlook 2013によってブロックされる場合にチェックします。
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a>パラメーター

 _pwszFileName_
  
> [in]添付ファイルのファイル名へのポインター。
    
 _pfBlocked_
  
> [out]指定した添付ファイルがブロック **されている場合は true** を示す値へのポインター。それ以外の場合は **false です**。
    
## <a name="see-also"></a>関連項目



[MAPI 定数](mapi-constants.md)
  
[添付ファイルがブロックされているのを確認する](how-to-verify-an-attachment-is-blocked.md)

