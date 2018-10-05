---
title: PidTagRtfSyncBodyTag 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyTag
api_type:
- COM
ms.assetid: 2dab5018-4214-4162-93bc-e5565f3ac24c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 24ef1d4e3e936426aea8216119e8ada9f6122e95
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387511"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a>PidTagRtfSyncBodyTag 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ テキストの先頭に表示される重要な文字が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RTF_SYNC_BODY_TAG、PR_RTF_SYNC_BODY_TAG_A、PR_RTF_SYNC_BODY_TAG_W  <br/> |
|識別子:  <br/> |0x1008  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI メッセージ  <br/> |
   
## <a name="remarks"></a>備考

[](rtfsync.md)関数は、メッセージ テキストの先頭を示すために、テキストのタグを使用します。 テキストが変更されると、前のテキストの先頭を検索するタグを使用します。 
  
これらのプロパティは、リッチ テキスト形式の補助プロパティです。 **** 関数で使用されて、クライアント アプリケーションで直接使用するものではありません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。
    
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

