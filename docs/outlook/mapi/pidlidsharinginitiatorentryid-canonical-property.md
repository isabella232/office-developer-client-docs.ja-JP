---
title: PidLidSharingInitiatorEntryId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorEntryId
api_type:
- COM
ms.assetid: 47f00706-83df-49cb-bda7-ef572d76a020
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6881f5ed54baffd37ff25d26f455b82bf2526d41
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802165"
---
# <a name="pidlidsharinginitiatorentryid-canonical-property"></a>PidLidSharingInitiatorEntryId の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
共有メッセージのプロパティとして指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidSharingInitiatorEid  <br/> |
|プロパティを設定します。  <br/> |PSETID_Sharing  <br/> |
|長い ID (LID):  <br/> |0x00008A09  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |共有  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、現在ログオンしているユーザーのアドレス帳の**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティの値を設定する必要があります ( [[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)を参照してください)。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> クライアント間でのメールボックスのフォルダーを共有します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
