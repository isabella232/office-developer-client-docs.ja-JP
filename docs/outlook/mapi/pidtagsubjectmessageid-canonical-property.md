---
title: PidTagSubjectMessageId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubjectMessageId
api_type:
- COM
ms.assetid: d4b1a087-0986-467a-aaa9-fc643f7c56fc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c89a0a86ac733cd2cce1efc071e47fcb011fec18
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573069"
---
# <a name="pidtagsubjectmessageid-canonical-property"></a>PidTagSubjectMessageId 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
レポートが生成されているメッセージからコピーされたバイナリ値が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SUBJECT_IPM  <br/> |
|識別子:  <br/> |0x0038  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI の封筒  <br/> |
   
## <a name="remarks"></a>注釈

レポートを元のメッセージに関連付けるには、 **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) のプロパティと同様に、このプロパティを使用できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

