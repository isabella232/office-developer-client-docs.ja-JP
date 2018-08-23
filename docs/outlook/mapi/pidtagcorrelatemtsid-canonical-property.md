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
ms.openlocfilehash: 468cda97398bc393b1c0a65e2c13df5ba3ade3aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568911"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a>PidTagCorrelateMtsid 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
レポートを送信したメッセージに関連づけるために使用するメッセージ転送システム (MTS) 識別子が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CORRELATE_MTSID  <br/> |
|識別子:  <br/> |0x0E0D  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>注釈

トランスポート プロバイダーでは、TRUE にこのプロパティのセットを使用して発信されたメッセージが検出されると、そのメッセージの MTS 識別子をこのプロパティを設定します。 伝送においては、次の個人間メッセージ (IPM) の [送信済みアイテム フォルダー内のメッセージにこのプロパティが格納されます。
  
X.400 など、MTS の id で関連付けをサポートしているメッセージング システムでは、元のメッセージとそれへの応答として生成されるすべてのレポートがトランスポート エンベロープの一部としての識別子を保持します。 レポートが配信されるとこのようなメッセージング システムから、トランスポート プロバイダーは、レポートのトランスポート エンベロープから MTS 識別子を元にこのプロパティを設定します。 このプロパティは、レポートと共に保存されます。
  
クライアント アプリケーションは、このプロパティを持つすべてのメッセージの検索結果のフォルダーを管理できます。 レポートは、このようなメッセージで、クライアントで検索結果フォルダーに制限を適用、メッセージの元のバージョンを検索し、新しい情報では、元のメッセージ情報を関連付けることができます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

