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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 00c07069ed174fe55556dfe48398d65b4e64100e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359228"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a>PidTagReceivedByAddressType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを実際に受信するメッセージング ユーザーの電子メール アドレスの種類 (SMTP など) が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECEIVED_BY_ADDRTYPE、PR_RECEIVED_BY_ADDRTYPE_A、PR_RECEIVED_BY_ADDRTYPE_W  <br/> |
|識別子:  <br/> |0x0075  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI 封筒  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、メッセージを実際に受信するメッセージング ユーザーのアドレス プロパティの例です。 これらは、受信トランスポート プロバイダーによって設定する必要があります。
  
アドレス型文字列には、大文字のアルファベット文字 A から Z、および 0 から 9 の数字のみを含めることができます。 これらのプロパティは **、PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) プロパティを修飾するため、SMTP などのアドレスの種類を指定して、アドレスを構築する方法を示します。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

