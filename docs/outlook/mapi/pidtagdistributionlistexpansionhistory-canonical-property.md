---
title: PidTagDistributionListExpansionHistory 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDistributionListExpansionHistory
api_type:
- HeaderDef
ms.assetid: fc1e0162-d655-4761-92e7-b469579c270b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 91d1554fab3b7ff21b5ad8d5d2546feb8c75758f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600149"
---
# <a name="pidtagdistributionlistexpansionhistory-canonical-property"></a>PidTagDistributionListExpansionHistory 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの送信中に配布リストが展開された方法を示す履歴が含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DL_EXPANSION_HISTORY  <br/> |
|識別子:  <br/> |0x0013  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 封筒  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、トランスポート プロバイダーがクライアント アプリケーションを設定している場合にクライアント アプリケーションを受信できます。 メッセージコンテンツがレポートと一緒に返される場合は、送信側クライアントでも使用できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagDistributionListExpansionProhibited 標準プロパティ](pidtagdistributionlistexpansionprohibited-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

