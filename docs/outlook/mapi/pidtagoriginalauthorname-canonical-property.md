---
title: PidTagOriginalAuthorName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorNam
api_type:
- COM
ms.assetid: beb23742-d844-4d90-9b13-1ad376d4206c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bb62f3a44c9f17070db969683891fb2e2d62eb5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355777"
---
# <a name="pidtagoriginalauthorname-canonical-property"></a>PidTagOriginalAuthorName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの最初のバージョンの作成者の表示名、つまり、転送または返信の前にメッセージを格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINAL_AUTHOR_NAME、PR_ORIGINAL_AUTHOR_NAME_A、PR_ORIGINAL_AUTHOR_NAME_W  <br/> |
|識別子:  <br/> |0x004d  <br/> |
|データの種類 :   <br/> |PT_UNICODE、PT_STRING8  <br/> |
|エリア:  <br/> |電子メール  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティは、メッセージの作成者のアドレスプロパティの例です。 最初にメッセージを送信したときに、クライアントアプリケーションはこれらのプロパティを**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) の値に設定する必要があります。 メッセージが転送または返信されるときには変更されません。
  
元の作成者のプロパティを使用すると、ローカルのメッセージングドメインの外部にある情報を保持できます。 インターネットからなど、他のメッセージングドメインからメッセージが到着すると、これらのプロパティを使用して元の情報が失われないようにすることができます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagDisplayName 標準プロパティ](pidtagdisplayname-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

