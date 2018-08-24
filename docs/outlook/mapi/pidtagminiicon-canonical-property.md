---
title: PidTagMiniIcon 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMiniIcon
api_type:
- HeaderDef
ms.assetid: a436b590-63f3-413c-a9c2-7664567e0ff0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5514e0553f719e2e875aad7001bb38a6a52e8e08
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589778"
---
# <a name="pidtagminiicon-canonical-property"></a>PidTagMiniIcon 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームの半分のサイズのアイコンのビットマップが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MINI_ICON  <br/> |
|識別子:  <br/> |0x0FFC  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、内容と同じアイコンの 32 × 32 ピクセルのイメージが含まれているのです。ICO ファイルですが、左上の 16 × 16 ピクセルだけは、重要と見なされます。 このプロパティは通常からコピーします。ICO ファイルが小さい行のフォーム構成ファイルの該当する [説明] セクションで指定されています。
  
 **メモ**いくつかのプラットフォームのサポート 16 × 16 ピクセル アイコンではない操作を行います。 32 × 32 の形式このプロパティは、このようなケースでは使用できませんが、クライアント アプリケーションは表示の矛盾に注意する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagIcon 標準プロパティ](pidtagicon-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

