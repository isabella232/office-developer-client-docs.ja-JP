---
title: PidTagBody 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 243a59798980d8c0cfaf1a726d6408dbd66ebba8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326636"
---
# <a name="pidtagbody-canonical-property"></a>PidTagBody 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージテキストが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_BODY、PR_BODY_A、PR_BODY_W  <br/> |
|識別子:  <br/> |0x1000  <br/> |
|データの種類 :   <br/> |PT_UNICODE、PT_STRING8  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティは、通常、個人間メッセージ (IPM) でのみ使用されます。 
  
リッチテキスト形式 (RTF) をサポートするメッセージストアは、メッセージテキスト内の空白への変更を無視します。 **PR_BODY**が初めて保存されると、メッセージストアは、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティ (RTF バージョンのメッセージテキスト) も生成して保存します。 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドが呼び出され、 **PR_BODY**が変更されている場合、メッセージストアは[rtfsync](rtfsync.md)関数を呼び出して RTF バージョンとの同期を確実に行います。 空白のみが変更された場合、プロパティは変更されません。 これにより、メッセージが rtf に対応していないクライアントおよびメッセージングシステムを経由するときに、重要な RTF 形式がすべて保持されます。 
  
このプロパティの値は、MAPI が実行されているオペレーティングシステムのコードページで記述する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagRtfInSync 標準プロパティ](pidtagrtfinsync-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

