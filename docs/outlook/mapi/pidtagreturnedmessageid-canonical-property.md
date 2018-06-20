---
title: PidTagReturnedMessageid の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 1f0f13e2-7554-41fc-a7a9-a90c34181c96
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8624821d264500a440b5988ffa30a5c31dc8a91f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803369"
---
# <a name="pidtagreturnedmessageid-canonical-property"></a>PidTagReturnedMessageid の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
Nonread レポートと元のメッセージが返される場合、TRUE が格納されます。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_RETURNED_IPM  <br/> |
|識別子:  <br/> |0x0033  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |MAPI の封筒  <br/> |
   
## <a name="remarks"></a>備考

X.400 トランスポート プロバイダーは、未読のレポートでこのプロパティを設定します。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

