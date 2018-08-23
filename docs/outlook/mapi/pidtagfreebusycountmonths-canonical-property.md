---
title: PidTagFreeBusyCountMonths 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyCountMonths
api_type:
- HeaderDef
ms.assetid: 278a77f2-65ec-4281-b406-942cc416a476
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e7dc8c06fca48c5f7c124a1fdf2228ebeb9da450
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569982"
---
# <a name="pidtagfreebusycountmonths-canonical-property"></a>PidTagFreeBusyCountMonths 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
パブリック フォルダーに公開する空き時間情報データの範囲の開始と終了日を計算するための値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FREEBUSY_COUNT_MONTHS  <br/> |
|識別子:  <br/> |0x6869  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |クラスによって定義されたメッセージ送信できます。  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの値が 0 以上にする必要があります 36 以下とします。 必須プロパティではありません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> ユーザーまたはリソースの可用性を発行します。
    
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
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

