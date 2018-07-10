---
title: PidTagIpmSentMailEntryId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSentMailEntryId
api_type:
- HeaderDef
ms.assetid: f6877435-6b26-4060-924f-a65591ad9538
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2bf7665d7867b9c7151f787bbc6b3cfd802bca35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802899"
---
# <a name="pidtagipmsentmailentryid-canonical-property"></a>PidTagIpmSentMailEntryId の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
標準的な個人間メッセージ (IPM) の [送信済みアイテム フォルダーのエントリ id が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_IPM_SENTMAIL_ENTRYID  <br/> |
|識別子:  <br/> |0x35E4  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>備考

、送信した個人間のメッセージは通常、送信済みアイテム フォルダーに配置されます。 クライアントは、送信されたメッセージの**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) のプロパティを設定するのにはこのプロパティを使用できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
