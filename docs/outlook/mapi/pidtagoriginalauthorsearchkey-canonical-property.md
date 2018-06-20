---
title: PidTagOriginalAuthorSearchKey の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorSearchKey
api_type:
- COM
ms.assetid: 4a10cf99-c5e6-4a24-b531-3aebb7800bfe
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e5b283376d018b7b2675e05f994d586126437590
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803052"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a>PidTagOriginalAuthorSearchKey の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
転送または返信する前にメッセージは、メッセージの最初のバージョンの作成者の検索キーが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ORIGINAL_AUTHOR_SEARCH_KEY  <br/> |
|識別子:  <br/> |0x0056  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、メッセージの作成者のアドレスのプロパティのいずれかです。 メッセージの最初の提出書類は、クライアント アプリケーションは、 **PR_SENDER_SEARCH_KEY**の[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)プロパティの値にこのプロパティを設定する必要があります。 メッセージを転送または返信するときは変更されません。 
  
ローカルのメッセージング ドメインの外部からの情報の保持の元の作成者プロパティを使用します。 別のメッセージング ドメインからメッセージが到着するなど、インターネットからこれらのプロパティは、元の情報が失われていないことを確認する方法。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

