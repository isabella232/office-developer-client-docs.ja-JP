---
title: PidTagOriginalSenderEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEntryId
api_type:
- COM
ms.assetid: bd182589-afea-4967-92f5-ba1914e4db3f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0b30a61d3bce6d1e6295edb1e93e27b9f7fc8363
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574446"
---
# <a name="pidtagoriginalsenderentryid-canonical-property"></a>PidTagOriginalSenderEntryId 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
最初のバージョンのメッセージを転送または返信する前にメッセージは、送信者のエントリ id が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINAL_SENDER_ENTRYID  <br/> |
|識別子:  <br/> |0x005B  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージの元の送信者のアドレスのプロパティのいずれかです。 メッセージの最初の提出書類は、クライアント アプリケーションは、 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) プロパティの値にこのプロパティを設定する必要があります。 メッセージを転送または返信するときは変更されません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
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

