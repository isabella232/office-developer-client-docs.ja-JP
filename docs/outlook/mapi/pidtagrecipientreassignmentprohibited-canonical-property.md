---
title: PidTagRecipientReassignmentProhibited の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0176485ca9b84260176e3be8ec9c8f42cf755cba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803291"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a>PidTagRecipientReassignmentProhibited の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
電子メール メッセージのメッセージを転送するときに追加の受信者を追加することが禁止されているかどうかを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_RECIPIENT_REASSIGNMENT_PROHIBITED  <br/> |
|識別子:  <br/> |0x002B  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |MAPI の封筒  <br/> |
   
## <a name="remarks"></a>備考

電子メール メッセージの**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) の値に基づいて、このプロパティが設定されます。 **PR_SENSITIVITY**が (機密) を"0x00"に、または省略することを追加することを意味、このプロパティを設定する必要があります"0x00000000"の (標準) または"0x00000003"に設定されて場合は、電子メール メッセージに受信者を追加または変更が許可されます。 メール オブジェクトの**PR_SENSITIVITY**は、(個人)"0x00000001"または"0x00000002"(プライベート) に設定されている場合は、このプロパティが"0x01"を設定する必要があります転送では、この電子メールの受信者を追加または変更を追加できないようにするのにします。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージの許可の操作を指定します。
    
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

