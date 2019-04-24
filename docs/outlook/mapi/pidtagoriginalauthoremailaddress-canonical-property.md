---
title: PidTagOriginalAuthorEmailAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEmailAddress
api_type:
- COM
ms.assetid: 67cda756-ba71-4f29-a601-55359e44d93b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7918c5d5b585ffb199bfbc140edfb8286b499b40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329240"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a>PidTagOriginalAuthorEmailAddress 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの最初のバージョンの作成者の電子メールアドレス、つまり転送または返信の前にメッセージを格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS、PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A、PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W  <br/> |
|識別子:  <br/> |0x007a  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |サーバー  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティは、メッセージの作成者のアドレスプロパティの例です。 クライアントアプリケーションは、最初にメッセージを送信するときに、これらのプロパティを**PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) プロパティの値に設定する必要があります。 メッセージが転送または返信されるときには変更されません。
  
元の作成者のプロパティを使用すると、ローカルのメッセージングドメインの外部にある情報を保持できます。 インターネットからなど、他のメッセージングドメインからメッセージが到着すると、これらのプロパティを使用して元の情報が失われないようにすることができます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

