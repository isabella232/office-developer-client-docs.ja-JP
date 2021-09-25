---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 174320928f94992c010e5c4349ba66e2ec6457cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614165"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プライベート ストアのキャッシュ Exchangeモードが有効になっているExchangeポリシーによって適用されるかどうかを示します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|次の方法でエクスポートされます。  <br/> |msmapi32.dll  <br/> |
|呼び出し元:  <br/> |Client  <br/> |
|実装元:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

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



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

