---
title: PidTagAcknowledgementMode 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAcknowledgementMode
api_type:
- HeaderDef
ms.assetid: 23329ca3-89f9-4e5a-9c8a-6262f2a2d26f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 28b42e6abee5d918dbcca69c13642f3ebcc859e1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581938"
---
# <a name="pidtagacknowledgementmode-canonical-property"></a>PidTagAcknowledgementMode 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージの受信確認モードの識別子が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ACKNOWLEDGEMENT_MODE  <br/> |
|識別子:  <br/> |0x0001  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、次の値の 1 つだけ持つことができます。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |手動受信を確認します。  <br/> |
|1  <br/> |自動受信を確認します。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

