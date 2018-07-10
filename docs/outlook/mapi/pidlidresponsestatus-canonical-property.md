---
title: PidLidResponseStatus の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0bfa3a01613c49b122e92e4ac281e5b20b5f07ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802139"
---
# <a name="pidlidresponsestatus-canonical-property"></a>PidLidResponseStatus の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
出席者の返信状況を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidResponseStatus  <br/> |
|プロパティを設定します。  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008218  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>備考

レスポンスのステータスは、次の表の値のいずれかである必要があります。
  
|**応答ステータス**|**値**|**説明**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |対応するこのオブジェクトの必要はありません。 これは、オブジェクトの予定および会議の応答オブジェクトの大文字と小文字です。  <br/> |
|respOrganized  <br/> |0x00000001  <br/> |この会議は、開催者に属しています。  <br/> |
|respTentative  <br/> |0x00000002  <br/> |出席者の会議では、この値は、出席者が会議出席依頼を仮承諾することを示します。  <br/> |
|respAccepted  <br/> |0x00000003  <br/> |出席者の会議 t には、この値は、出席者が会議出席依頼を受け入れることを示します。  <br/> |
|respDeclined  <br/> |0x00000004  <br/> |出席者の会議では、この値は、出席者が会議出席依頼を辞退したことを示します。  <br/> |
|respNotResponded  <br/> |0x00000005  <br/> |出席者の会議では、この値は、出席者がまだ応答していないことを示します。 この値は、会議出席依頼、会議の更新、および会議の取り消しにします。  <br/> |
   
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
