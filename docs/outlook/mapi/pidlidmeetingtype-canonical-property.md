---
title: PidLidMeetingType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidMeetingType
api_type:
- COM
ms.assetid: 290b290c-7836-4a7e-bf1a-8d0225a07e56
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e61ce7798c9e41dbb707d0d5773b116f7cce02d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802039"
---
# <a name="pidlidmeetingtype-canonical-property"></a>PidLidMeetingType 標準プロパティ

  
  
**適用対象**: Outlook 
  
会議出席依頼または会議の更新の種類を示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidMeetingType  <br/> |
|プロパティを設定します。  <br/> |PSETID_Meeting  <br/> |
|長い ID (LID):  <br/> |0x00000026  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの値を次のいずれかに設定する必要があります。
  
|**プロパティ**|**値**|**説明**|
|:-----|:-----|:-----|
|mtgEmpty  <br/> |0x00000000  <br/> |指定されていません。  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |最初の会議出席依頼の場合。  <br/> |
|mtgFull  <br/> |0x00010000  <br/> |フル更新します。  <br/> |
|mtgInfo  <br/> |0x00020000  <br/> |情報を更新します。  <br/> |
|mtgOutOfDate  <br/> |0x00080000  <br/> |この後に新しい会議出席依頼または会議の更新を受信しました。  <br/> |
|mtgDelegatorCopy  <br/> |0x00100000  <br/> |これは、委任者の場合、デリゲートのハンドルの会議に関連するオブジェクトに設定されています。  <br/> |
   
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
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

