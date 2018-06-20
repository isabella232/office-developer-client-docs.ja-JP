---
title: PidTagOriginalAuthorAddressType の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorAddressType
api_type:
- COM
ms.assetid: 7cdedb1a-e441-469b-be50-2f18203eb30d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fb30f2b29691984614891e2345fe97abe6316f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803044"
---
# <a name="pidtagoriginalauthoraddresstype-canonical-property"></a>PidTagOriginalAuthorAddressType の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
転送または返信する前にメッセージは、メッセージの最初のバージョンの作成者のアドレスの種類が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ORIGINAL_AUTHOR_ADDRTYPE、PR_ORIGINAL_AUTHOR_ADDRTYPE_A、PR_ORIGINAL_AUTHOR_ADDRTYPE_W  <br/> |
|識別子:  <br/> |0x0079  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティでは、メッセージの作成者のアドレスのプロパティの例を示します。 メッセージの最初の提出書類は、クライアント アプリケーションは、 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) プロパティの値にこのプロパティを設定する必要があります。 メッセージを転送または返信するときは変更されません。
  
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

