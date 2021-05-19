---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5e623c9d40ffd2dd276bd9601676244644bb3402
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417708"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a>GetDefCachedModeDownloadPubFoldFavs

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
パブリック フォルダーのお気に入りフォルダーのExchange キャッシュ モードを有効にするかどうか、およびこれがポリシーによって適用されるかどうかを示します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|次の方法でエクスポートされます。  <br/> |msmapi32.dll  <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|実装元:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a>パラメーター

 _pfPolicy_
  
> [out] **戻** り値がポリシーによって適用される場合は **true、適用** されていない場合は false。 
    
## <a name="return-values"></a>戻り値

 **true**
  
- キャッシュが有効です。
    
 **false**
  
- キャッシュは無効です。
    
## <a name="see-also"></a>関連項目



[GetDefCachedMode](getdefcachedmode.md)

