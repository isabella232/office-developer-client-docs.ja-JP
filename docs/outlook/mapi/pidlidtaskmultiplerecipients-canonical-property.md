---
title: PidLidTaskMultipleRecipients の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1e1cba3d927072cb03dbd34eee518c9b0a9e0383
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802224"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a>PidLidTaskMultipleRecipients の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
タスクの受信者についての最適化のヒントを提供します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidTaskMultRecips  <br/> |
|プロパティを設定します。  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008120  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>備考

かどうかこのオプションを設定すると、この必要がありますプロパティに次の値の 0 個以上のビットごとの**OR**演算されます。 
  
|**名前**|**値**|**説明**|
|:-----|:-----|:-----|
|Sent  <br/> |0x00000001  <br/> |タスクには、複数の主な受信者があります。  <br/> |
|Received  <br/> |0x00000002  <br/> |送信済みアイテムのヒントは存在しませんでした、ですが、タスクが複数の主な受信者を持っているクライアントを検出しました。  <br/> |
|Reserved  <br/> |0x00000004  <br/> |この値は予約されています。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

