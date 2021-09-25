---
title: PidTagCorrelateMtsid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagCorrelateMtsid
api_type:
- HeaderDef
ms.assetid: d0fc4e91-ed90-4d27-bd23-f01e99728e2d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 113fcb076d730ab63e7fbe6874a5cb4f77fb6565
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616531"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a>PidTagCorrelateMtsid 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
レポートと送信メッセージを関連付ける場合に使用されるメッセージ転送システム (MTS) 識別子が含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CORRELATE_MTSID  <br/> |
|識別子:  <br/> |0x0E0D  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>注釈

トランスポート プロバイダーは、このプロパティが TRUE に設定された送信済みメッセージを検出すると、このプロパティをそのメッセージの MTS 識別子に設定します。 送信後、このプロパティは、メッセージと一緒に対人間メッセージ (IPM) 送信アイテム フォルダーに格納されます。
  
X.400 などの MTS 識別子による相関関係をサポートするメッセージング システムは、元のメッセージのトランスポート エンベロープの一部として識別子を保持し、そのメッセージに応答して生成されたレポートも保持します。 このようなメッセージング システムからレポートが配信される場合、トランスポート プロバイダーは、このプロパティをレポートのトランスポート エンベロープから元の MTS 識別子に設定します。 このプロパティは、レポートと一緒に格納されます。
  
クライアント アプリケーションは、このプロパティを持つすべてのメッセージの検索結果フォルダーを維持できます。 このようなメッセージのレポートが表示される場合、クライアントは検索結果フォルダーに制限を適用し、元のバージョンのメッセージを見つけて、元のメッセージ情報と新しい情報を関連付けることができます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

