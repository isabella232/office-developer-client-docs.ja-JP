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
ms.openlocfilehash: a8f88e4b41ab455c55bfd1cb36b73ce7ef0383b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348994"
---
# <a name="pidlidfshouldtnef-canonical-property"></a>PidLidFShouldTNEF 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アイテムをトランスポートニュートラルカプセル化形式 (TNEF) でエンコードするかどうかを示します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidfid tnef  <br/> |
|プロパティセット:  <br/> |PSETID_Common  <br/> |
|ロング ID (LID):  <br/> |0x000085a5  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |実行時の構成  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、Microsoft Word が電子メールエディターとして設定されているときに設定され、リッチテキスト形式 (RTF) のストリームに埋め込まれている OLE オブジェクトを送信します。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]] 
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

