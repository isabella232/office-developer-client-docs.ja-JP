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
ms.openlocfilehash: 2868533e0383309e013bb82aaa4300a0a40e335a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577514"
---
# <a name="pidtagcontrolid-canonical-property"></a>PidTagControlId 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ダイアログ ボックスで使用されているコントロールの一意の識別子が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTROL_ID  <br/> |
|識別子:  <br/> |0x3F07  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI 表示テーブル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、コントロールの一意の識別子が含まれています。 この識別子には、 [GUID](guid.md)の構造体と、 **LONG**型のバイナリ値を含める必要があります。 ダイアログ ボックス内のすべてのコントロールは、サービス プロバイダーを識別するのには、同じ**GUID**を使用する必要があり、各コントロールは、一意で使用する**コントロールが競合していないことを確認します**。 
  
このプロパティは、通知で使用されます。 などのディスプレイ テーブルに送信された通知は、更新するコントロールを一意に識別するには、このプロパティを設定する必要があります。 
  
## <a name="related-resources"></a>関連リソース

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

