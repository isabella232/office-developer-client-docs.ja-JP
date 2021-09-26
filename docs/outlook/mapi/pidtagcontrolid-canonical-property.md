---
title: PidTagControlId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 163a7e88bdb6f6c22a608af2b5a0af961f033779
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583508"
---
# <a name="pidtagcontrolid-canonical-property"></a>PidTagControlId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ダイアログ ボックスで使用されるコントロールの一意の識別子を含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTROL_ID  <br/> |
|識別子:  <br/> |0x3F07  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 表示テーブル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、コントロールの一意の識別子が含まれる。 この識別子には [、GUID](guid.md) 構造と LONG 型のバイナリ値が含 **まれている必要があります**。 ダイアログ ボックス内のすべてのコントロールは同じ **GUID** を使用してサービス プロバイダーを識別し、各コントロールは一意の **LONG** 値を使用してコントロールが衝突しない必要があります。 
  
このプロパティは、通知で使用されます。 たとえば、表示テーブルに送信される通知は、更新するコントロールを一意に識別するためにこのプロパティを設定する必要があります。 
  
## <a name="related-resources"></a>関連リソース

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

