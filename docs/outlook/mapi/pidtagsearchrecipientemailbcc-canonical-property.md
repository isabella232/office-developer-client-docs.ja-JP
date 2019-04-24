---
title: PidTagSearchRecipientEmailBcc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9561d13-8d52-500c-5369-15a2cf5c92c3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5b0db4b3bc7903aae74fa7275d3e27e22d628514
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359158"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a>PidTagSearchRecipientEmailBcc 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ストア上の未送信メッセージの**BCC**行に指定されている受信者の電子メールアドレスまたは表示名の一覧で、クエリが行われている Unicode 文字列が格納されています。 
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SEARCH_RECIP_EMAIL_BCC_W  <br/> |
|識別子:  <br/> |0x0EA8  <br/> |
|プロパティの種類:  <br/> |PT_UNICODE  <br/> |
|接続  <br/> |検索  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、送受信されたメッセージには BCC 情報が含まれていないため、送信されていないストアのメッセージのみに関連します。
  
> [!NOTE]
> この MAPI 制限タグは、ブラインドカーボンコピーとしてメッセージが送信される電子メールアドレスまたは表示名を検索するときに使用されますが、現在所有しているダウンロード可能なヘッダーファイルでは定義されていない場合があります。 コードに追加するには、次の値を使用します。 >`#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> 検索フォルダーリストの構成を操作するためのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

