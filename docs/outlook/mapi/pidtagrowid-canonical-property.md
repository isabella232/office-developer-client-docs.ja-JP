---
title: PidTagRowid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowid
api_type:
- COM
ms.assetid: 0fdcb55a-2971-4c7d-b61e-7ada2d19d0e6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8d58342e0460352bd9d260cb6e73de358cb2fc23
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387721"
---
# <a name="pidtagrowid-canonical-property"></a>PidTagRowid 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者テーブルまたはステータス テーブル内で受信者の一意の識別子が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ROWID  <br/> |
|識別子:  <br/> |0x3000  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |一般的な MAPI  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、テーブルを所有するオブジェクトの有効期間にのみ有効な一時的な値です。 テーブルの列として表示されますが、保存されていません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> 順序と、クライアントとサーバー間のデータ転送のフローを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

