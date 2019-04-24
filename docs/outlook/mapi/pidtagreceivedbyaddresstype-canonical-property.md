---
title: PidTagReceivedByAddressType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByAddressType
api_type:
- COM
ms.assetid: 0eef299d-6923-4dae-9a18-91ea82ea0f3e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 00c07069ed174fe55556dfe48398d65b4e64100e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359228"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a>PidTagReceivedByAddressType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
実際にメッセージを受信するメッセージングユーザーの電子メールアドレスの種類 (SMTP など) を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECEIVED_BY_ADDRTYPE、PR_RECEIVED_BY_ADDRTYPE_A、PR_RECEIVED_BY_ADDRTYPE_W  <br/> |
|識別子:  <br/> |0x0075  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI エンベロープ  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティは、実際にメッセージを受信するメッセージングユーザーのアドレスプロパティの例です。 これらは、受信トランスポートプロバイダーによって設定される必要があります。
  
アドレスの種類の文字列には、a ~ Z の英字と 0 ~ 9 の数字を含めることができます。 これらのプロパティは、SMTP などのアドレスの種類を指定することによって、 **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) プロパティを修飾し、アドレスの構築方法を示します。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージに対して許容されるプロパティと操作を指定します。
    
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

