---
title: PidTagSwappedToDoStore 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoStore
api_type:
- COM
ms.assetid: 1edae9ac-fc9a-4bfe-b053-99de848c5144
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 41aa97a52176cf68775d6fd507d3d042888092cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358906"
---
# <a name="pidtagswappedtodostore-canonical-property"></a>PidTagSwappedToDoStore 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
電子メールの送信後処理の必要性を決定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SWAPPED_TODO_STORE  <br/> |
|識別子:  <br/> |0x0E2C  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 送信不可  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティが下書きメッセージに設定されている場合、その値はメッセージの **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) プロパティの値に設定する必要があります。
  
詳細については [、「[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) 」セクション「フラグが設定されたメッセージの送信後処理」を参照してください。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> フラグに関連するプロパティと操作を指定します。
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> メールなどのオブジェクトアラームのプロパティと対話モデルを指定します。
    
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

