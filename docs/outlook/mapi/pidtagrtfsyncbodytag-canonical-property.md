---
title: PidTagRtfSyncBodyTag 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRtfSyncBodyTag
api_type:
- COM
ms.assetid: 2dab5018-4214-4162-93bc-e5565f3ac24c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9f4fe42e99eedfd8f77cbc6ac55aa8b59873f8d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555105"
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
   
## <a name="remarks"></a>注釈

[RTFSync 関数は](rtfsync.md)、テキスト タグを使用してメッセージ テキストの先頭を示します。 テキストを変更すると、タグを使用して前のテキストの先頭を検索します。 
  
これらのプロパティは、リッチ テキスト形式の補助プロパティです。 これらは **RTFSync 関数によって使用** され、クライアント アプリケーションによって直接使用される意図はありません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。
    
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

