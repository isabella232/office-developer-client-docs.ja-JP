---
title: IAttachmentSecurityIsAttachmentBlocked
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity.IsAttachmentBlocked
api_type:
- COM
ms.assetid: 6986d27a-9602-e44a-0797-4c47f2184ef7
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: d255d7b6e80fe0c080fa0a27a7976db758a8c2ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439780"
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

