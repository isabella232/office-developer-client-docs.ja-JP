---
title: PidLidAppointmentTimeZoneDefinitionEndDisplay 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: facbcb9eed18db304cac334be845c0b3869ba508
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574805"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a>PidLidAppointmentTimeZoneDefinitionEndDisplay 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
単独の予定または会議出席依頼の終了時刻が選択されているときに使用されるタイム ゾーンの説明を格納する[TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx)構造体の保存形式に対応するストリームが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidApptTZDefEndDisplay  <br/> |
|プロパティを設定します。  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x0000825F  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |予定表  <br/> |
   
## <a name="remarks"></a>注釈

2003 または以前のバージョンを Microsoft Office Outlook とソリューションにコラボレーション データ オブジェクト (CDO) 1.2.1 を置くし、Outlook または Microsoft Exchange Server では、予定表更新ツールを実行していないことは、シングル ・ インスタンスの終了時刻と開始時刻を格納します。予定および会議出席依頼で世界協定時刻 (UTC)。 これらのクライアントは、予定または会議出席依頼を作成する場所のタイム ゾーンの情報を格納していません。
  
Outlook または Exchange Server の予定表を実行している Microsoft Office Outlook 2007 では、CDO 1.2.1 に基づくソリューションの以降の Microsoft Outlook のバージョンでは、終了時刻のタイム ゾーンを格納する使用**dispidApptTZDefEndDisplay**ツールを更新します。 **dispidApptTZDefEndDisplay**は、[スケジュールされた、タイム ゾーンの規則を変更する場合に、終了時刻を調整する必要があるかどうかを判断する元のタイム ゾーンで、予定または会議を示しています。 このプロパティが存在しない場合は、 **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) のプロパティで指定されたタイム ゾーンが使用されます。 **DispidApptTZDefStartDisplay**が存在しないか無効の場合は、現在のローカル タイム ゾーンと見なされます。 **dispidApptTZDefEndDisplay**は、表示目的でのみ使用され、定期的なアイテムの展開で使用されていません。 
  
パーサーは、 **dispidApptTZDefEndDisplay**から取得したストリームを読み取るとき、または**dispidApptTZDefEndDisplay**などのバイナリのプロパティへの取り組みのためのストリームに**TZDEFINITION**が引き続き発生する場合注意が必要である必要があります。 詳細については、[バイナリのプロパティをコミットするためのストリームに永続化する TZDEFINITION](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)を参照してください。
  
 **dispidApptTZDefEndDisplay**は、 **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) のプロパティのタイム ゾーン情報を指定します。 形式、制約、および**dispidApptTZDefEndDisplay**の計算は、 **dispidApptTZDefStartDisplay**プロパティで指定されたと同じです。 
  
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

