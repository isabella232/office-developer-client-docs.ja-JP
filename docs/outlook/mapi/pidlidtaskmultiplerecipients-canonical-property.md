---
title: PidLidTaskMultipleRecipients 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMultipleRecipients
api_type:
- COM
ms.assetid: 28ba9997-72dd-465f-94a7-35a317a361ef
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3b260917e107086dee6176f73b6c82c3a1825327
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391172"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a>PidLidTaskMultipleRecipients 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
タスクの受信者についての最適化のヒントを提供します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskMultRecips  <br/> |
|プロパティを設定します。  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008120  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>備考

かどうかこのオプションを設定すると、この必要がありますプロパティに次の値の 0 個以上のビットごとの**OR**演算されます。 
  
|**名前**|**値**|**説明**|
|:-----|:-----|:-----|
|Sent  <br/> |0x00000001  <br/> |タスクには、複数の主な受信者があります。  <br/> |
|Received  <br/> |0x00000002  <br/> |送信済みアイテムのヒントは存在しませんでした、ですが、タスクが複数の主な受信者を持っているクライアントを検出しました。  <br/> |
|Reserved  <br/> |0x00000004  <br/> |この値は予約されています。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

