---
title: PidTagSearchRecipientEmailCc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 38fe217d-cf2e-51de-c97a-acb015129fd3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 03501e14740d7b27bd54d761ae701e8863ad79dd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392838"
---
# <a name="pidtagsearchrecipientemailcc-canonical-property"></a>PidTagSearchRecipientEmailCc 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
照会中の電子メール アドレスまたはストア内のメッセージの [ **CC** ] 行でアドレス指定された受信者の表示名の一覧で、Unicode 文字列が含まれています。 
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SEARCH_RECIP_EMAIL_CC_W  <br/> |
|識別子:  <br/> |0x0EA7  <br/> |
|プロパティの種類:  <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |検索  <br/> |
   
## <a name="related-resources"></a>関連リソース

> [!NOTE]
> この MAPI 制限のタグ、電子メール アドレスを検索するか、カーボン コピーとしてメッセージを送信する名前を表示するときに使用しない、現在あるダウンロード可能なヘッダー ファイルで定義できます。 次の値を使用して、コードに追加できます >。`#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`
  
### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> プロパティや検索フォルダーの一覧の構成を操作するための動作を指定します。
    
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

