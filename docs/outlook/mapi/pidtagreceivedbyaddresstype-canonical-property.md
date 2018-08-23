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
ms.openlocfilehash: cd7a287a2240d372edf6cca6bac522266c0ca620
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581168"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a>PidTagReceivedByAddressType 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
電子メール アドレスの種類、SMTP など、メッセージング ユーザーに実際にメッセージが表示されますが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECEIVED_BY_ADDRTYPE、PR_RECEIVED_BY_ADDRTYPE_A、PR_RECEIVED_BY_ADDRTYPE_W  <br/> |
|識別子:  <br/> |0x0075  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MAPI の封筒  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティでは、実際にメッセージを受信するメッセージング ユーザーのアドレスのプロパティの例を示します。 着信トランスポート プロバイダーが設定されなければなりません。
  
アドレスの種類の文字列には、のみ、大文字のアルファベット文字 A から Z、および 0 から 9 までの番号を含めることができます。 これらのプロパティは、アドレスの構築方法を示すため、SMTP などのアドレスの種類を指定することによって、 **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) のプロパティを修飾します。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージの許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

