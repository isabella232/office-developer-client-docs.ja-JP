---
title: PidLidFExceptionalAttendees の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalAttendees
api_type:
- COM
ms.assetid: f1f489a3-e83a-4e96-bf9a-d98bc17d29f5
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7c7f654d42df7856b0e69bf276a763ccd29d1d87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801961"
---
# <a name="pidlidfexceptionalattendees-canonical-property"></a>PidLidFExceptionalAttendees の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
このプロパティは、1 つまたは複数の例外の定期的な予定表オブジェクトを少なくとも 1 つの RecipientRow には、埋め込まれている例外メッセージの少なくとも 1 つかどうかを示します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidFExceptionalAttendees  <br/> |
|プロパティを設定します。  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x0000822B  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>備考

値の false の場合、または、このプロパティがない場合は、カレンダー オブジェクトが例外を含んでいないか、または埋め込まれている例外メッセージは、RecipientRows のことを示します。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

