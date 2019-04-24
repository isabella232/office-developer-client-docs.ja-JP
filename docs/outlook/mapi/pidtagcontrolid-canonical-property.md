---
title: PidTagControlId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b27f59e0bfdcac8eca1751af2f07139f12e2b3a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334742"
---
# <a name="pidtagcontrolid-canonical-property"></a>PidTagControlId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ダイアログボックスで使用されるコントロールの一意識別子を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTROL_ID  <br/> |
|識別子:  <br/> |0x3f07  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 表示テーブル  <br/> |
   
## <a name="remarks"></a>解説

このプロパティには、コントロールの一意の識別子が含まれています。 この識別子には、 [GUID](guid.md)構造と、 **LONG**型のバイナリ値を含める必要があります。 ダイアログボックス内のすべてのコントロールは、同じ**GUID**を使用してサービスプロバイダーを識別する必要があり、各コントロールは固有の**LONG**値を使用して、コントロールが競合しないようにする必要があります。 
  
このプロパティは通知で使用されます。 たとえば、表示テーブルで送信された通知では、更新するコントロールを一意に識別するために、このプロパティを設定する必要があります。 
  
## <a name="related-resources"></a>関連リソース

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

