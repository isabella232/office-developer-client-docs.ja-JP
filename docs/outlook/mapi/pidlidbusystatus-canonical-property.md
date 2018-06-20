---
title: PidLidBusyStatus の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusyStatus
api_type:
- COM
ms.assetid: 50c91fe6-2a61-4348-a16d-fd5c501b0715
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 926f0425a4a59cad4280917573c974375c94f50b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801833"
---
# <a name="pidlidbusystatus-canonical-property"></a>PidLidBusyStatus の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
予定の有無を表します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidBusyStatus  <br/> |
|プロパティを設定します。  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008205  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |カレンダー  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、オブジェクトが記載されているイベントで、ユーザーの可用性を指定し、以下に指定した値のいずれかである必要があります。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |予定なし。  <br/> |
|0x00000001  <br/> |ユーザーは、予定されている仮の予定のイベントです。  <br/> |
|0x00000002  <br/> |予定あり。  <br/> |
|0x00000003  <br/> |外出中。  <br/> |
   
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

