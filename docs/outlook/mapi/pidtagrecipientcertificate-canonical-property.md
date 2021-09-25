---
title: PidTagRecipientCertificate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRecipientCertificate
api_type:
- COM
ms.assetid: 7c5c749e-5463-4935-85b5-32219d06f782
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 88a3b93229f2a2f405da8467225eeabfc1441c5a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624665"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a>PidTagRecipientCertificate 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
レポートで使用するメッセージ受信者の ASN.1 証明書が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECIPIENT_CERTIFICATE  <br/> |
|識別子:  <br/> |0x0C13  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 受信者  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、レポートで使用する受信者PR_USER_CERTIFICATE **(** [PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) プロパティのコピーです。 これは、受信者がメッセージを実際に受信したと発信者に証明するために使用できます。配信レポートは必ずしも示すとは限りません。
  
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

