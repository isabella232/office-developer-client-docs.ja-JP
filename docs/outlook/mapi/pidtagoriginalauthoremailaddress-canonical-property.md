---
title: PidTagOriginalAuthorEmailAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginalAuthorEmailAddress
api_type:
- COM
ms.assetid: 67cda756-ba71-4f29-a601-55359e44d93b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 670ebb8a50de98eaa9310bc3632cbb2b3e14e33e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599925"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a>PidTagOriginalAuthorEmailAddress 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの最初のバージョンの作成者の電子メール アドレス(転送または返信前のメッセージ)が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS、PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A、PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W  <br/> |
|識別子:  <br/> |0x007A  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |サーバー  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、メッセージの作成者のアドレス プロパティの例です。 メッセージの最初の送信時に、クライアント アプリケーションは、これらのプロパティを PR_SENDER_EMAIL_ADDRESS ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) プロパティ **の** 値に設定する必要があります。 メッセージが転送または返信された場合は、変更されません。
  
元の作成者プロパティを使用すると、ローカル メッセージング ドメイン外からの情報を保持できます。 インターネットなどの別のメッセージング ドメインからメッセージが到着すると、これらのプロパティを使用して、元の情報が失われなかねない方法が提供されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

