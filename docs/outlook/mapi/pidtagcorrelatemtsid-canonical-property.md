---
title: PidTagCorrelateMtsid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelateMtsid
api_type:
- HeaderDef
ms.assetid: d0fc4e91-ed90-4d27-bd23-f01e99728e2d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 96bfc184752b6a3e15434ad67ac8c2b4b26cac4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359935"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a>PidTagCorrelateMtsid 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信されたメッセージにレポートを関連付けるために使用されるメッセージ転送システム (MTS) 識別子を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CORRELATE_MTSID  <br/> |
|識別子:  <br/> |0x0e0d  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>解説

このプロパティが TRUE に設定されている送信済みメッセージがトランスポートプロバイダーによって検出されると、そのメッセージの MTS 識別子にこのプロパティが設定されます。 送信後、このプロパティはメッセージと共に、IPM (個人間メッセージ) の送信済みアイテムフォルダーに格納されます。
  
MTS 識別子による関連付けをサポートするメッセージングシステム (たとえば、X)。識別子は、元のメッセージのトランスポートエンベロープの一部として、また、それに対する応答で生成されたレポートの一部として保持されます。 このようなメッセージングシステムからレポートが配信されると、トランスポートプロバイダーは、このプロパティをレポートのトランスポートエンベロープから元の MTS 識別子に設定します。 その後、このプロパティはレポートと共に保存されます。
  
クライアントアプリケーションは、このプロパティを持つすべてのメッセージの検索結果フォルダーを維持できます。 このようなメッセージのレポートがある場合、クライアントは検索結果フォルダーに制限を適用し、元のバージョンのメッセージを検索し、元のメッセージ情報を新しい情報に関連付けることができます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

