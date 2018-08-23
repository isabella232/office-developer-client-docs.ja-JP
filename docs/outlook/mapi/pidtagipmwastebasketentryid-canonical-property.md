---
title: PidTagIpmWastebasketEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmWastebasketEntryId
api_type:
- HeaderDef
ms.assetid: 0f8dd043-66f0-4193-9b95-853bc3827f73
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 66bbf49d737c42ecc2f6c765a60540163649f447
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573895"
---
# <a name="pidtagipmwastebasketentryid-canonical-property"></a>PidTagIpmWastebasketEntryId 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
標準的な個人間メッセージ (IPM) の [削除済みアイテム フォルダーのエントリ id が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_IPM_WASTEBASKET_ENTRYID  <br/> |
|識別子:  <br/> |0x35E3  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>注釈

クライアント アプリケーションは、個人間のメッセージを削除を削除済みアイテム フォルダーに移動します。 このフォルダーにメッセージがある場合、またはこのプロパティがサポートされていない場合は、クライアントはメッセージを削除する必要があります。 
  
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

