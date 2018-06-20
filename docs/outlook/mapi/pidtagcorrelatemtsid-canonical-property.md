---
title: PidTagCorrelateMtsid の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 57da2d4c78914323b5dafa4f5ba5b7628d0e2f2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802653"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a>PidTagCorrelateMtsid の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
レポートを送信したメッセージに関連づけるために使用するメッセージ転送システム (MTS) 識別子が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_CORRELATE_MTSID  <br/> |
|識別子:  <br/> |0x0E0D  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>備考

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
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

