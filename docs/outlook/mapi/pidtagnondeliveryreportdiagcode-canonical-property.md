---
title: PidTagNonDeliveryReportDiagCode 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagNonDeliveryReportDiagCode
api_type:
- HeaderDef
ms.assetid: a39c0f54-bdca-498f-a75c-dd8702e5385a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ed0196f88ca5295dba109743d60c1e59c33c53b3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583339"
---
# <a name="pidtagnondeliveryreportdiagcode-canonical-property"></a>PidTagNonDeliveryReportDiagCode 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
非送信レポートの一部を形成する診断コードが含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_NDR_DIAG_CODE  <br/> |
|識別子:  <br/> |0x0C05  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、次のいずれかの値を指定できます。
  
MAPI_DIAG_ALPHABETIC_CHARACTER_LOST 
  
> 
    
MAPI_DIAG_CONTENT_SYNTAX_IN_ERROR 
  
> 
    
MAPI_DIAG_CONTENT_TOO_LONG 
  
> 
    
MAPI_DIAG_CONTENT_TYPE_UNSUPPORTED 
  
> 
    
MAPI_DIAG_CONVERSION_LOSS_PROHIB 
  
> 
    
MAPI_DIAG_CONVERSION_UNSUBSCRIBED 
  
> 
    
MAPI_DIAG_CRITICAL_FUNC_UNSUPPORTED 
  
> 
    
MAPI_DIAG_EITS_UNSUPPORTED 
  
> 
    
MAPI_DIAG_EXPANSION_FAILED 
  
> 
    
MAPI_DIAG_EXPANSION_PROHIBITED 
  
> 
    
MAPI_DIAG_IMPRACTICAL_TO_CONVERT 
  
> 
    
MAPI_DIAG_LENGTH_CONSTRAINT_VIOLATD 
  
> 
    
MAPI_DIAG_LINE_TOO_LONG 
  
> 
    
MAPI_DIAG_LOOP_DETECTED 
  
> 
    
MAPI_DIAG_MAIL_ADDRESS_INCOMPLETE 
  
> 
    
MAPI_DIAG_MAIL_ADDRESS_INCORRECT 
  
> 
    
MAPI_DIAG_MAIL_FORWARDING_PROHIB 
  
> 
    
MAPI_DIAG_MAIL_FORWARDING_UNWANTED 
  
> 
    
MAPI_DIAG_MAIL_NEW_ADDRESS_UNKNOWN 
  
> 
    
MAPI_DIAG_MAIL_OFFICE_INCOR_OR_INVD 
  
> 
    
MAPI_DIAG_MAIL_ORGANIZATION_EXPIRED 
  
> 
    
MAPI_DIAG_MAIL_RECIPIENT_DECEASED 
  
> 
    
MAPI_DIAG_MAIL_RECIPIENT_DEPARTED 
  
> 
    
MAPI_DIAG_MAIL_RECIPIENT_MOVED 
  
> 
    
MAPI_DIAG_MAIL_RECIPIENT_TRAVELLING 
  
> 
    
MAPI_DIAG_MAIL_RECIPIENT_UNKNOWN 
  
> 
    
MAPI_DIAG_MAIL_REFUSED 
  
> 
    
MAPI_DIAG_MAIL_UNCLAIMED 
  
> 
    
MAPI_DIAG_MAXIMUM_TIME_EXPIRED 
  
> 
    
MAPI_DIAG_MTS_CONGESTED 
  
> 
    
MAPI_DIAG_MULTIPLE_INFO_LOSSES 
  
> 
    
MAPI_DIAG_NO_BILATERAL_AGREEMENT 
  
> 
    
MAPI_DIAG_NO_DIAGNOSTIC 
  
> 
    
MAPI_DIAG_NUMBER_CONSTRAINT_VIOLATD 
  
> 
    
MAPI_DIAG_OR_NAME_AMBIGUOUS 
  
> 
    
MAPI_DIAG_OR_NAME_UNRECOGNIZED 
  
> 
    
MAPI_DIAG_PAGE_TOO_LONG 
  
> 
    
MAPI_DIAG_PARAMETERS_INVALID 
  
> 
    
MAPI_DIAG_PICTORIAL_SYMBOL_LOST 
  
> 
    
MAPI_DIAG_PROHIBITED_TO_CONVERT 
  
> 
    
MAPI_DIAG_PUNCTUATION_SYMBOL_LOST 
  
> 
    
MAPI_DIAG_REASSIGNMENT_PROHIBITED 
  
> 
    
MAPI_DIAG_RECIPIENT_UNAVAILABLE 
  
> 
    
MAPI_DIAG_REDIRECTION_LOOP_DETECTED 
  
> 
    
MAPI_DIAG_RENDITION_UNSUPPORTED 
  
> 
    
MAPI_DIAG_SECURE_MESSAGING_ERROR 
  
> 
    
MAPI_DIAG_SUBMISSION_PROHIBITED 
  
> 
    
MAPI_DIAG_TOO_MANY_RECIPIENTS 
  
> 
    
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagNonDeliveryReportReasonCode 標準プロパティ](pidtagnondeliveryreportreasoncode-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

