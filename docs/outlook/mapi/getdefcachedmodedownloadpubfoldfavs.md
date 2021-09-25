---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 602d9ce178c0d88192d3eaba899b15f6c2445c8d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580175"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a>GetDefCachedModeDownloadPubFoldFavs

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[パブリック フォルダーのお気に入Exchangeキャッシュ モード]が有効になっているかどうか、およびこれがポリシーによって適用されるかどうかを示します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|次の方法でエクスポートされます。  <br/> |msmapi32.dll  <br/> |
|呼び出し元:  <br/> |Client  <br/> |
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

