---
title: PidTagSensitivity 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSensitivity
api_type:
- COM
ms.assetid: 5b678475-f2a8-4831-ad68-11654e09c821
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 93be3351749ac3e9d285fb214f746d58b55fb5b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803521"
---
# <a name="pidtagsensitivity-canonical-property"></a>PidTagSensitivity 標準プロパティ

  
  
**適用対象**: Outlook 
  
メッセージの秘密度のメッセージの送信者の意見を示す値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SENSITIVITY  <br/> |
|識別子:  <br/> |0x0036  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>注釈

メッセージ オブジェクトがこのプロパティを公開することをお勧めします。
  
このプロパティは、次の値の 1 つだけ持つことができます。
  
SENSITIVITY_NONE 
  
> メッセージには、特別な区別はありません。
    
SENSITIVITY_PERSONAL 
  
> メッセージは個人用です。
    
SENSITIVITY_PRIVATE 
  
> 専用のメッセージです。
    
SENSITIVITY_COMPANY_CONFIDENTIAL 
  
> メッセージには、会社の機密情報が指定されます。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
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

