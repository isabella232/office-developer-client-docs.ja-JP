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
ms.openlocfilehash: 45e4362fc025c1784e9432c5d641e865a044bd00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800411"
---
# <a name="iattachmentsecurityisattachmentblocked"></a>IAttachmentSecurity::IsAttachmentBlocked

  
  
**適用されます**: Outlook 
  
指定した添付ファイルが表示して、インデックス作成の Microsoft Outlook 2010 または Microsoft Outlook 2013 でブロックされているかどうかを確認します。
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a>Parameters

 _pwszFileName_
  
> [in]添付ファイルのファイル名へのポインター。
    
 _pfBlocked_
  
> [out]ポインターの値を示す**true の**場合は、指定した添付ファイルはブロックされます。それ以外の場合、 **false を指定**します。
    
## <a name="see-also"></a>関連項目



[MAPI �萔](mapi-constants.md)
  
[添付ファイルがブロックされていることを確認します。](how-to-verify-an-attachment-is-blocked.md)

