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
ms.openlocfilehash: c659b77767fddc4c783732082c2eb65c68af8dbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356715"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a>PidTagRecipientCertificate 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
レポートで使用するためのメッセージ受信者の ASN. 1 証明書が保存されています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECIPIENT_CERTIFICATE  <br/> |
|識別子:  <br/> |0x0c13  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 受信者  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、レポートで使用する受信者の**PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) プロパティのコピーです。 このメソッドを使用すると、受信者が実際にメッセージを受信したことを証明することができます。これは、配信レポートが必ずしも示しているわけではありません。
  
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

