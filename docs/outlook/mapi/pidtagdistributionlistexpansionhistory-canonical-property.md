---
title: PidTagDistributionListExpansionHistory 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDistributionListExpansionHistory
api_type:
- HeaderDef
ms.assetid: fc1e0162-d655-4761-92e7-b469579c270b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a172fa1e04f1ea50c29955febda47be6e52663b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422958"
---
# <a name="pidtagdistributionlistexpansionhistory-canonical-property"></a>PidTagDistributionListExpansionHistory 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ送信中に配布リストが展開された方法を示す履歴が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DL_EXPANSION_HISTORY  <br/> |
|識別子:  <br/> |0x0013  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI エンベロープ  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、トランスポートプロバイダーが設定している場合は、クライアントアプリケーションを受信するために使用できます。 また、メッセージの内容がレポートと共に返される場合は、送信側クライアントでも使用できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagDistributionListExpansionProhibited 標準プロパティ](pidtagdistributionlistexpansionprohibited-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

