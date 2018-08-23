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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cbe1915df46010c5574065826ac1814f45c8c093
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803652"
---
# <a name="pidtagswappedtodostore-canonical-property"></a>PidTagSwappedToDoStore 標準プロパティ

  
  
**適用対象**: Outlook 
  
必要性を決定するの転送、電子メールの処理後です。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SWAPPED_TODO_STORE  <br/> |
|識別子:  <br/> |0x0E2C  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI 以外から送信できます。  <br/> |
   
## <a name="remarks"></a>注釈

下書きメッセージにこのプロパティが設定されている場合は、メッセージの**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) のプロパティの値にその値を設定する必要があります。
  
詳細については、 [[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)を参照してくださいセクション"送信後フラグ付きメッセージの処理します」。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> プロパティ フラグに関連する操作を指定します。
    
[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> 電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。
    
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

