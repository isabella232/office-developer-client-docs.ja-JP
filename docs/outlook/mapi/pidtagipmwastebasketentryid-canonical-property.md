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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3794386c4461c90f973e4028132cb8220dfaa19b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426353"
---
# <a name="pidtagipmwastebasketentryid-canonical-property"></a>PidTagIpmWastebasketEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
標準の対人間メッセージ (IPM) 削除済みアイテム フォルダーのエントリ識別子を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_IPM_WASTEBASKET_ENTRYID  <br/> |
|識別子:  <br/> |0x35E3  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>注釈

クライアント アプリケーションは、削除された対人メッセージを削除済みアイテム フォルダーに移動する必要があります。 メッセージが既にこのフォルダーにある場合、またはこのプロパティがサポートされていない場合、クライアントはメッセージを削除する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

