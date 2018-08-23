---
title: PidLidFShouldTNEF 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFShouldTNEF
api_type:
- COM
ms.assetid: 3cab23b6-f0e3-4703-a83b-12a617537651
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ad9d81342ed749b6b1b640fd8118519aae7469a4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595175"
---
# <a name="pidlidfshouldtnef-canonical-property"></a>PidLidFShouldTNEF 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
トランスポート ニュートラル カプセル化形式 (TNEF) を持つアイテムをエンコードするかどうかを示します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidFShouldTNEF  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x000085A5  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |実行時の構成  <br/> |
   
## <a name="remarks"></a>注釈

電子メール エディターとして Word を設定し、リッチ テキスト形式 (RTF) のストリームに埋め込まれている OLE オブジェクトを送信するとき、このプロパティが設定されています。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[MS OXPROPS] 
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

