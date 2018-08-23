---
title: PidTagStoreRecordKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreRecordKey
api_type:
- COM
ms.assetid: 27347302-bd52-4f62-98f1-6c37f9a66463
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4598ca5e654308f7701b1dd66adb227599773b7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803609"
---
# <a name="pidtagstorerecordkey-canonical-property"></a>PidTagStoreRecordKey 標準プロパティ

  
  
**適用対象**: Outlook 
  
バイナリ比較の一意の識別子 (キーのレコード) オブジェクトが格納されているメッセージ ストアが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STORE_RECORD_KEY  <br/> |
|識別子:  <br/> |0x0FFA  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>注釈

メッセージ ・ ストアのこのプロパティは、ストアの**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) のプロパティと同じです。
  
このプロパティと**PR_RECORD_KEY**間の関係は、 **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) と**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) との間の関係と同じです。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。
    
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

