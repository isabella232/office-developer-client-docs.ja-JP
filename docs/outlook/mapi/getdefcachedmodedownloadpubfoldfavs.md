---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ced6f2c6540e04a0bb4945ff98c4fda520322f03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581728"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a>GetDefCachedModeDownloadPubFoldFavs

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
**パブリック フォルダーのお気に入り**フォルダーの Exchange キャッシュ モードが有効になっているかどうか、ポリシーによって適用されるには、これかどうかを示します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|によってエクスポートされます。  <br/> |msmapi32.dll  <br/> |
|によって呼び出されます。  <br/> |クライアント  <br/> |
|によって実装されます。  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a>パラメーター

 _pfPolicy_
  
> [out]**true**でない場合、ポリシーでは、 **false を指定**して、戻り値が設定されている場合です。 
    
## <a name="return-values"></a>戻り値

 **true**
  
- キャッシュを有効にします。
    
 **false**
  
- キャッシュを無効にします。
    
## <a name="see-also"></a>関連項目



[GetDefCachedMode](getdefcachedmode.md)

