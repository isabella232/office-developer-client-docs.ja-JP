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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: eab8ce71d28a672d7069a1c16da5cd2cc2e149f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342505"
---
# <a name="pidtagsensitivity-canonical-property"></a>PidTagSensitivity 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの送信者のメッセージの感度に関する意見を示す値を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SENSITIVITY  <br/> |
|識別子:  <br/> |0x0036  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

メッセージ オブジェクトでこのプロパティを公開する必要があります。
  
このプロパティには、次のいずれかの値を指定できます。
  
SENSITIVITY_NONE 
  
> メッセージに特別な区別はありません。
    
SENSITIVITY_PERSONAL 
  
> メッセージは個人用です。
    
SENSITIVITY_PRIVATE 
  
> メッセージはプライベートです。
    
SENSITIVITY_COMPANY_CONFIDENTIAL 
  
> メッセージは、会社の機密として指定されます。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
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

