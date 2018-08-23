---
title: PidTagAttachMimeSequence 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMimeSequence
api_type:
- HeaderDef
ms.assetid: d2a84f24-b4a5-4e16-9219-7a579a31a8f8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b8fe0dd61247d3473db4cc728ecfa2c83682b691
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587720"
---
# <a name="pidtagattachmimesequence-canonical-property"></a>PidTagAttachMimeSequence 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MIME メッセージの添付ファイルの MIME のシーケンス番号が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_MIME_SEQUENCE  <br/> |
|識別子:  <br/> |0x3710  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |メッセージの添付ファイルのプロパティ  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティが使用される MHTML をサポートするためです。 MIME メッセージの MIME のマルチパートのボディ部の親内の添付ファイルのシーケンス番号を表します。
  
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

