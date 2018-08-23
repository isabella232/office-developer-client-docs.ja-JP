---
title: PidTagSpamThreshold 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2b2d6b8e-e3dd-4a9b-8bb5-53add675605d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a9a5e72a585a2af8914b858cb4d174899706797e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566776"
---
# <a name="pidtagspamthreshold-canonical-property"></a>PidTagSpamThreshold 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
スパムのフィルタ リングのレベルを示す long 値。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SPAM_THRESHOLD  <br/> |
|長い ID (LID):  <br/> | 0x041B  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |スパム  <br/> |
   
## <a name="values"></a>Values

スパム フィルターの値は次のとおりです。
  
|**スパム レベル**|**値**|
|:-----|:-----|
|なし  <br/> |0 xffffffff  <br/> |
|低  <br/> |0x00000006  <br/> |
|中  <br/> |0x00000005  <br/> |
|高  <br/> |0x00000003  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> 許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。
    
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

