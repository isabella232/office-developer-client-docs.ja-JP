---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7595fac4346a537eed86550432f56a761c27c0ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800190"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**適用されます**: Outlook 
  
プライベートの Exchange ストアの Exchange キャッシュ モードが有効になっているかどうか、ポリシーによって適用されるには、これかどうかを示します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|によってエクスポートされます。  <br/> |msmapi32.dll  <br/> |
|によって呼び出されます。  <br/> |クライアント  <br/> |
|によって実装されます。  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a>Parameters

 _pfPolicy_
  
> [out]**true**でない場合、ポリシーでは、 **false を指定**して、戻り値が設定されている場合です。 
    
## <a name="return-values"></a>戻り値

 **true**
  
- キャッシュを有効にします。
    
 **false**
  
- キャッシュを無効にします。
    
## <a name="see-also"></a>関連項目



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

