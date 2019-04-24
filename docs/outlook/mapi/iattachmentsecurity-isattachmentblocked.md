---
title: iattachmentsecurityisattachmentblocked ブロックされました
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350849"
---
# <a name="iattachmentsecurityisattachmentblocked"></a>IAttachmentSecurity::IsAttachmentBlocked

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定された添付ファイルが microsoft outlook 2010 または microsoft outlook 2013 によってブロックされているかどうかを確認し、表示およびインデックスを作成します。
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a>パラメーター

 _pwszFileName_
  
> 順番添付ファイルのファイル名へのポインター。
    
 _pfblocked_
  
> 読み上げ指定された添付ファイルがブロックされている場合は**true**を示す値へのポインター。それ以外の場合は**false**。
    
## <a name="see-also"></a>関連項目



[MAPI 定数](mapi-constants.md)
  
[添付ファイルがブロックされていることを確認する](how-to-verify-an-attachment-is-blocked.md)

