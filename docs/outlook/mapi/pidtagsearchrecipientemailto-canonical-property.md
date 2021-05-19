---
title: PidTagSearchRecipientEmailTo 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f5de77c3-5912-f7bc-8e8c-3a053545c359
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d254df132db5542ce5235c1c3ab42ea768399f0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358920"
---
# <a name="pidtagsearchrecipientemailto-canonical-property"></a>PidTagSearchRecipientEmailTo 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ストア上のメッセージの宛先行でアドレス指定されている受信者の電子メール アドレスまたは表示名の一覧でクエリされている Unicode文字列が含まれます。 
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SEARCH_RECIP_EMAIL_TO_W  <br/> |
|識別子:  <br/> |0x0EA6  <br/> |
|プロパティの種類:  <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |検索  <br/> |
   
## <a name="related-resources"></a>関連リソース

> [!NOTE]
> この MAPI 制限タグは、メッセージが送信される電子メール アドレスまたは表示名を検索するときに使用され、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。 次の値を使用して、コードに追加できます。>  `#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`
  
### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのMicrosoft Exchange Server提供します。
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> 検索フォルダー 一覧の構成を操作するためのプロパティと操作を指定します。
    
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

