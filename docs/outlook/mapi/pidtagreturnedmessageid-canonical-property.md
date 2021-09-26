---
title: PidTagReturnedMessageid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1f0f13e2-7554-41fc-a7a9-a90c34181c96
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f68df73ab071e1fb0108d54f518dbc34ce7f5c1c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599566"
---
# <a name="pidtagreturnedmessageid-canonical-property"></a>PidTagReturnedMessageid 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
元のメッセージが読み取り以外のレポートで返される場合は TRUE を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RETURNED_IPM  <br/> |
|識別子:  <br/> |0x0033  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |MAPI 封筒  <br/> |
   
## <a name="remarks"></a>注釈

X.400 トランスポート プロバイダーは、未読レポートにこのプロパティを設定します。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

