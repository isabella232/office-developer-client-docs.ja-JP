---
title: imapiforminfoopenformcontainer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.OpenFormContainer
api_type:
- COM
ms.assetid: 1d6eec99-59f9-4700-9b83-7f7f8787a9f8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a76d0c554d7cf06aceeaa2925c199e45411b999d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342092"
---
# <a name="imapiforminfoopenformcontainer"></a>IMAPIFormInfo::OpenFormContainer

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のフォームがインストールされているフォームコンテナーへのポインターを返します。
  
```cpp
HRESULT OpenFormContainer(
  LPMAPIFORMCONTAINER FAR * ppformcontainer
);
```

## <a name="parameters"></a>パラメーター

 _ppformcontainer_
  
> 読み上げ返される form container オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="see-also"></a>関連項目



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

