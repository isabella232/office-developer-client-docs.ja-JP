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
ms.openlocfilehash: 05e29f01747e4d5aa2fe0b61e58fa2ba738a53fd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592851"
---
# <a name="pidtagoriginalauthorname-canonical-property"></a>PidTagOriginalAuthorName 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
転送または返信する前にメッセージは、メッセージの最初のバージョンの作成者の表示名が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINAL_AUTHOR_NAME、PR_ORIGINAL_AUTHOR_NAME_A、PR_ORIGINAL_AUTHOR_NAME_W  <br/> |
|識別子:  <br/> |0x004D  <br/> |
|データの種類 :   <br/> |PT_UNICODE、PT_STRING8  <br/> |
|領域:  <br/> |メール  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティでは、メッセージの作成者のアドレスのプロパティの例を示します。 メッセージの最初の提出書類は、クライアント アプリケーションは、 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) の値にこれらのプロパティを設定する必要があります。 メッセージを転送または返信するときは変更されません。
  
ローカルのメッセージング ドメインの外部からの情報の保持の元の作成者プロパティを使用します。 別のメッセージング ドメインからメッセージが到着するなど、インターネットからこれらのプロパティは、元の情報が失われていないことを確認する方法。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagDisplayName 標準プロパティ](pidtagdisplayname-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

