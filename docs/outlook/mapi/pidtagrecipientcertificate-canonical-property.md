---
title: PidTagRecipientCertificate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientCertificate
api_type:
- COM
ms.assetid: 7c5c749e-5463-4935-85b5-32219d06f782
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 464db3d360f6e872ac28f8d7cbec842d8b521f7e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585116"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a>PidTagRecipientCertificate 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
レポートで使用するため、メッセージの受信者の ASN.1 の証明書が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECIPIENT_CERTIFICATE  <br/> |
|識別子:  <br/> |0x0C13  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI 受信者  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、レポートで使用するための受信者の**PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) のプロパティのコピーです。 受信者が、メッセージは、配信レポートが必ずしも実際に受け取ったことを発信者に証明するために使用できます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

